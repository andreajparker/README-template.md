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

## Prerequisites

Before you begin, ensure you have met the following requirements:
<!--- These are just example requirements. Add, duplicate or remove as required --->
* You have installed the latest version of `<coding_language/dependency/requirement_1>`
* You have a `<Windows/Linux/Mac>` machine. State which OS is supported/which is not.
* You have read `<guide/link/documentation_related_to_project>`.

## Using <project_name>

To use <project_name>, follow these steps:
1. **Train** on your data
2. **Build/Rebuild** your image (run `.docker/build_image.sh` to rebuild the image)
3. **Deploy** the kubectl apply -f .docker/pod.yaml 

### Training
Talk about training: where is <project_name> trained? What data is used for training and how do you access that data? If you need to preprocess the data before it goes into the model link to any relevant preprocessing documentation (scripts, Confluence pages, etc.) here.

### Requirements for training
See **Prerequisites**

### Retraining <project_name>
<!--- These are just example requirements. Add or remove as required --->

To change the code or data:

1. Run `.docker/build_image.sh` to rebuild the image
2. Deploy the pod with `kubectl apply -f .docker/pod.yaml`

## Model input

Include a few sentences about what goes into your <project_name>/model.

```
<usage_example_1>
```

```
{
  "file_id": "FILE_ID_STRING",
  "regex_pred": "REGEX_PREDICTION_STRING"
}
```

Add commands and examples you think users will find useful. 

## <project_name> Output

<project_name>'s output includes `predicted_value`, as a string, and the confidence score of the prediction as a float. The allowed `predicted_value`s are defined in the `PREDICTED_VALUES` in `configuration.py`.

```
{
  "predicted_value": "PREDICTED_VALUE_STRING",
  "predicted_score": pred_score_float
}
````

<project_name>'s output is sent to `<database>/<S3 bucket>/<other data location>` and is used by `<downstream_application>` to `<predict_something>`

## Logging, Monitoring and Alerting

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

See the [Confluence page](https://link.to.confluence.page) for details on <project_name>'s monitoring and alerting.
