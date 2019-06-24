# AlexaSkillTemplates

Templates for the [ASK CLI](https://developer.amazon.com/docs/smapi/quick-start-alexa-skills-kit-command-line-interface.html) to quickly generate Alexa Skills. Create a quick-start skill from a template using the ASK CLI tool:

```
ask new --url http://AlexaSkillTemplates.com/index.json
```

### Example

The example below shows the workflow of creating an Alexa Skill using the **[alexa-app-bootstrap](https://github.com/matt-kruse/alexa-app-bootstrap)** module template. After using the `ask new` command, the skill is instantly deployable with no changes.

However, in a real situation, you would want to go into `src/index.js` to customize the skill name, invocation name, and behavior, then deploy.

<pre>
PS C:\workspace> ask new --url http://AlexaSkillTemplates.com/index.json
? List of templates you can choose <b style="color:red;">Alexa-App Bootstrap</b>
? Please type in your skill name:  <b style="color:red;">alexa-example</b>
[Warn]: Downloading skill template from unofficial resource. Please make sure you understand what each script is doing to best protect yourself from malicious usage
? Would you still like to continue execution ? <b style="color:red;">Yes</b>
Skill "alexa-example" has been created based on the chosen template
[Info]: Could not find hooks folder, creating a new hooks folder and downloading scripts.
PS C:\workspace> <b style="color:red;">cd alexa-example</b>
PS C:\workspace\alexa-example> <b style="color:red;">node deploy.js</b>
Using ask-cli to deploy the skill. Please wait for output...
###########################
##### pre-deploy hook #####
###########################
Codebase (src) built successfully.
###########################
Profile for the deployment: [default]
-------------------- Create Skill Project --------------------
Skill Id: amzn1.ask.skill.6c7ccae8-8653-4657-ac19-xxxxxxxxxxxx
Skill metadata deploy finished.
Model deployment finished.
Lambda deployment finished.
Lambda function(s) created:
  [Lambda ARN] arn:aws:lambda:us-east-1:xxxxxxxxxxxx:function:ask-example-skill
[Info]: No in-skill product to be deployed.
Your skill is now deployed and enabled in the development stage. Try simulate your Alexa skill skill using "ask dialog" command.
PS C:\workspace\alexa-example>
</pre>


