# MediChat Health Bot Container

A medical chatbot assistance service that allows patients to make health-related inquiries in real-time within a web-chat environment. The solution seeks to bridge the gap between patients & their access to health services by giving patients quality healthcare at the convenience of their homes.It allows users to communicate with the [Azure Health Bot](https://azure.microsoft.com/en-us/services/bot-services/health-bot/) through a WebChat interface.


1.Deploy the website:

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FJoachim-Wambua%2FMediChatApp%2Fmaster%2Fazuredeploy.json)

2.Set the following environment variables:

`APP_SECRET`

`WEBCHAT_SECRET`

3.Configure scenario invocation:

The Health Bot service uses [language models](https://docs.microsoft.com/HealthBot/language_model_howto) to interpret end user utterances and trigger the relevant scenario logic in response.

4.Set the Bot service direct line channel endpoint (optional)

In some cases it is required to set the endpoint URI so that it points to a specific geography. The geographies supported by the bot service each have a unique direct line endpoint URI:

- `directline.botframework.com` routes your client to the nearest datacenter. This is the best option if you do not know where your client is located.
- `asia.directline.botframework.com` routes only to Direct Line servers in Eastern Asia.
- `europe.directline.botframework.com` routes only to Direct Line servers in Europe.
- `northamerica.directline.botframework.com` routes only to Direct Line servers in North America.

Pass your preferred geographic endpoint URI by setting the environment variable: `DIRECTLINE_ENDPOINT_URI` in your deployment. If no variable is found it will default to `directline.botframework.com`

**Note:** If you are deploying the code sample using the "Deploy to Azure" option, you should add the above secrets to the application settings for your App Service.