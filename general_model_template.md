# Project name

<!--- These are examples. See https://shields.io for others or to customize this set of shields. You might want to include dependencies, project status and licence info here --->
![GitHub repo size](https://img.shields.io/github/repo-size/scottydocs/README-template.md)
![GitHub contributors](https://img.shields.io/github/contributors/scottydocs/README-template.md)
![Jenkins](https://jenkins-badges.readthedocs.io/en/latest/_images/coverage_green.svg)

(Add other [coverage](https://shields.io/category/coverage), [build](https://shields.io/category/build), or [monitoring](https://shields.io/category/monitoring) badges if applicable to this project.)

Project name is a `<utility/tool/feature>` that allows `<insert_target_audience>` to do `<action/task_it_does>`.

Additional line of information text about what the project does. Your introduction should be around 2 or 3 sentences. Don't go overboard, people won't read it.

## Model Spec

* __Model Name__: your-model
* __Model Version__: v0.1.8
* __Production Model Endpoint__: `https://ambassador.someurl.com/seldon/seldon-system/your-model/api/v0.1/predictions`
* __Development Model Endpoint__: `https://dev-ambassador.someurl.com/seldon/seldon-system/your-model/api/v0.1/predictions`
* __Throughput Considerations__: `batch_size`

See **Model Input** and **Model Output** sections below for model input and output.

# Prerequisites

Before you begin, ensure you have met the following requirements:
<!--- These are just example requirements. Add, duplicate or remove as required --->
* You have installed the latest version of `<coding_language/dependency/requirement>`
* You have permissions for `<service/IAM_role/database>`
* You have read `<guide/link/documentation_related_to_project>`

# Using <project_name>

To use <project_name>, follow these steps:
1. **Train** - one or two sentences about training process
2. **Build** - one or two sentences about build process
3. **Deploy** - one or two setences about the deployment process

# Training, building and deploying

## Training

Include a few sentences about training your model here: where is <project_name> trained? What data is used for training and how does one access that data? For training the model, what was done and why? What _wasn't_ done? / What are some limitations of the current model?

Include a few sentences about preprocessing the data (if applicable); include links to any relevant preprocessing documentation (repos/scripts, Notebooks, Confluence pages, etc.).

## Building

Talk about building your model here in a few sentences.
 - If Rest API / Seldon: What steps (if any) does a user need to take to build the model? Jenkins should build the model-serving Docker image and push it to ECR.
 - If Lambda: talk about any relevant details here such as the Lambda function handler, tf-environment including any aditional resources such as IAM, SNS, etc.
 - If Queue (SQS) service: talk about the SQS queue messages (the input to the ML model), the predictions (SNS), and anything else you think might be useful.

## Deployment
Talk about deploying your model here in a few sentences.
 - If Seldon: talk about deploying the model to the EKS cluster and any relevant links ArgoCD and Helm resources.
 - If Lambda: Jenkins pipeline will automatically deploy the main branch in the model repo, but add anything else you think might be useful here.
 - If Queue (SQS) service: talk about Helm charts and anything else you think might be useful here.

# Model Inputs and Outputs

## Model input

Include a few sentences about what goes into your <project_name>/model.

```
{
  "file_id": "FILE_ID_STRING",
  "regex_pred": "REGEX_PREDICTION_STRING",
  ...
}
```

<project_name>'s input takes in `file_id` as as string, `regex_pred` as a string, and so on.

Provide a definition for any field names in the input data that are unclear, e.g., `regex_pred` is the carrier predicted by the regex heuristic.

## Model Output

<project_name>'s output includes `predicted_value`, as a string, and the confidence score of the prediction as a float. The allowed `predicted_value`s are defined in the `PREDICTED_VALUES` in `configuration.py`.

```
{
  "predicted_value": "PREDICTED_VALUE_STRING",
  "predicted_score": pred_score_float,
  ...
}
````

<project_name>'s output is sent to `<database>/<S3 bucket>/<other data location>` and is used by `<downstream_application>` to `<predict_something>`

Provide a definition for any field names in the output data that are unclear.


# Logging, Monitoring and Alerting

<project_name>'s logging messages are designed to make it easier:
- for engineers to debug
- for ops team to determine the issue and decide if engineering resource is needed

Currently <project_name>'s predictions and logs are sent to <database> and <monitoring tool> with the following values:
- file id
- model predicted value
- model predicted score
- model version name
- datetime when the prediction was generated 
that allows them to be tracked and filtered.

Monitors for <project_name> are setup in [Datadog](https://app.datadoghq.com/this_is_a_fake_link). An alert is sent via Slack if an <project_name> <action> fails.

See the [<project_name> Monitoring - Confluence page](https://link.to.confluence.page) for details on <project_name>'s monitoring and alerting.
