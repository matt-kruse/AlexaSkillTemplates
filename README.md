# AlexaSkillTemplates

Templates for the ASK CLI to quickly generate Alexa Skills. Create a quick-start skill from a template using the ASK CLI tool:

```
ask new --url http://AlexaSkillTemplates.com/index.json
```

### Example

The example below shows the workflow of creating an Alexa Skill using the alexa-app-bootstrap template. After using the `ask new` command, the skill is instantly deployable with no changes.

However, in a real situation, you would want to go into `src/index.js` to customize the skill name, invocation name, and behavior, then deploy.

```
PS C:\workspace> ask new --url http://AlexaSkillTemplates.com/index.json
? List of templates you can choose *Alexa-App Bootstrap*
? Please type in your skill name:  *alexa-example*
[Warn]: Downloading skill template from unofficial resource. Please make sure you understand what each script is doing to best protect yourself from malicious usage
? Would you still like to continue execution ? *Yes*
Skill "alexa-example" has been created based on the chosen template
[Info]: Could not find hooks folder, creating a new hooks folder and downloading scripts.
PS C:\workspace> *cd alexa-example*
PS C:\workspace\alexa-example> *node deploy.js*
Using ask-cli to deploy the skill. Please wait for output...
###########################
##### pre-deploy hook #####
###########################
Codebase (src) built successfully.
###########################
Profile for the deployment: [default]
-------------------- Create Skill Project --------------------
Skill Id: amzn1.ask.skill.6c7ccae8-8653-4657-ac19-b6a8fe432518
Skill metadata deploy finished.
Model deployment finished.
Lambda deployment finished.
Lambda function(s) created:
  [Lambda ARN] arn:aws:lambda:us-east-1:664201294062:function:ask-example-skill
[Info]: No in-skill product to be deployed.
Your skill is now deployed and enabled in the development stage. Try simulate your Alexa skill skill using "ask dialog" command.
PS C:\workspace\alexa-example>
```

