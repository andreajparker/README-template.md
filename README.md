# Project name

<!--- These are examples. See https://shields.io for others or to customize this set of shields. You might want to include dependencies, project status and licence info here --->
![GitHub repo size](https://img.shields.io/github/repo-size/scottydocs/README-template.md)
![GitHub contributors](https://img.shields.io/github/contributors/scottydocs/README-template.md)
![Jenkins](https://jenkins-badges.readthedocs.io/en/latest/_images/coverage_green.svg)

(Add other [coverage](https://shields.io/category/coverage), [build](https://shields.io/category/build), or [monitoring](https://shields.io/category/monitoring) badges if applicable to this project.)

Project name is a `<utility/tool/feature>` that allows `<insert_target_audience>` to do `<action/task_it_does>`.

Additional line of information text about what the project does. Your introduction should be around 2 or 3 sentences. Don't go overboard, people won't read it.

## Prerequisites

Before you begin, ensure you have met the following requirements:
<!--- These are just example requirements. Add, duplicate or remove as required --->
* You have installed the latest version of `<coding_language/dependency/requirement_1>`
* You have a `<Windows/Linux/Mac>` machine. State which OS is supported/which is not.
* You have read `<guide/link/documentation_related_to_project>`.

## Installing <project_name>

To install <project_name>, follow these steps:

Linux and macOS:
```
<install_command>
```

Windows:
```
<install_command>
```
## Using <project_name>

To use <project_name>, follow these steps:

```
<usage_example>
```

Add run commands and examples you think users will find useful. Provide an options reference for bonus points!

## Output

<project_names>'s output is sent to `<database>/<S3 bucket>/<other data location>` and is used by `<downstream_application>` to `<predict_something>`.

## Logging, Monitoring and Alerting

<project_name>'s logging messages are designed to make it easier:
- for engineers to debug
- for ops team to determine the issue and decide if engineering resource is needed

Currently <project_name>'s predictions and logs are sent to <database> and <monitoring tool> with the following values:
- file id
- model predicted value
- model version name
- datetime when the prediction was generated 
that allows them to be tracked and filtered.

Monitors for <project_name> are setup in [Datadog](https://app.datadoghq.com/this_is_a_fake_link). An alert is sent via Slack if an <project_name> <action> fails.

See the [Confluence page](https://link.to.confluence.page) for details on <project_name>'s monitoring and alerting.
