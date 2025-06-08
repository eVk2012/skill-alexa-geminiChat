# Alexa GeminiChat (es-ES)
### Plantilla de Skills de Alexa para integrar Google Gemini en dispositivos Alexa

**Creditos a [Scintilla Hub](https://www.youtube.com/@scintillahub) visitalos en YouTube**

## Requisitos

* Con una cuenta de Google genere una llave de autorización en el sitio del API [Google AI Developer](https://ai.google.dev/). Copie y guarde la llave, esta será visible solo en el momento de la creación.
* Cree una cuenta en [Amazon](https://www.amazon.com/ap/signin?openid.pape.preferred_auth_policies=Singlefactor&clientContext=132-2293245-7926858&openid.pape.max_auth_age=7200000&openid.return_to=https%3A%2F%2Fdeveloper.amazon.com%2Falexa%2Fconsole%2Fask&openid.identity=http%3A%2F%2Fspecs.openid.net%2Fauth%2F2.0%2Fidentifier_select&openid.assoc_handle=amzn_dante_us&openid.mode=checkid_setup&marketPlaceId=ATVPDKIKX0DER&openid.claimed_id=http%3A%2F%2Fspecs.openid.net%2Fauth%2F2.0%2Fidentifier_select&openid.ns=http%3A%2F%2Fspecs.openid.net%2Fauth%2F2.0&) y registrece en el login para la consola de _Alexa Developer Console_.

## Creando la Skill Alexa
Cree una Skill Alexa-hosted (Python) para Alexa: (_Create Skill_)

1. Name your Skill: Escoja un nombre de su preferencia (Ex: GeminiGPT)
2. Choose a primary locale: Español (US)
3. Clic en _Next_. En tipo de experiencia seleccione: Other > Custom > _Alexa-hosted (Python)_
4. _Hosting region_: Puede dejar en _US East (N. Virginia)_
5. En _Templates_: Clic en _Import Skill_
6. Inserte el enlace al repositorio: [https://github.com/Machally/skill-alexa-geminiChat.git](https://github.com/esamudio24/skill-alexa-geminiChat.git) y confirme.

## Configurando a Skill
Al finalizar la importación en _Invocations_ > _Skill Invocation Name_:
1. Edite _Skill Invocation Name_. Este será el comando de invocaión para su skill. Tome en cuenta los requisitos e restricciones de palabras
2. Clic en _Save_
3. Realize el Build de la Skill haciendo clic en _Build Skill_. Al finalizar, diríjase a la pestaña de **Code**
4. Cree un archivo dentro de la carpeta Lambda nombrelo _.env_ y agregue la línea, para el API key generada:
   ```shell
   GOOGLE_API_KEY=SuApiKeyGoogleAI
   ```
5. Clic en _Save_ y luego en _Deploy_
   
## Prueba de la Skill
Al finalizar el _deploy_ diríjase a la pestaña de **Test**:
1. En _Skill testing is enabled in_ cambielo de _Off_ a _Development_
2. Para usar comandos de voz acepte el requisito de uso de micrófono solicitado por el sitio, y para hablar haga clic y mantenga presionado el ícono de micrófono🎤, y suelte para enviar.
3. Utilice el comando de activación configurado para iniciar la habilidad y estará listo para interactuar con Gemini a través de Alexa.

La habilidad ahora estará disponible en todos los dispositivos Alexa vinculados a su cuenta.
