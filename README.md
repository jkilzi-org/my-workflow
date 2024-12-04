# F05EB00E.D9D7.46B1.BC27.136EB02E22E1

A basic workflow

## Prerequisites
* Java 11+ is installed.
* Apache Maven 3.8.6 or later is installed.
* [Quarkus CLI](https://quarkus.io/guides/cli-tooling) or [Knative Workflow CLI](https://kiegroup.github.io/kogito-docs/serverlessworkflow/latest/testing-and-troubleshooting/kn-plugin-workflow-overview.html) 0.21.3 or later is installed.
* (Optional) Docker is installed.
* (Optional) Podman is installed.
* (Optional) Kubernetes CLI is installed.
* Visual Studio Code with [Red Hat Java Extension](https://marketplace.visualstudio.com/items?itemName=redhat.java) and 
[Red Hat Serverless Workflow Editor](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-extension-serverless-workflow-editor) 
are installed to edit your workflows.

## References
* [About OpenShift Serverless Logic](https://openshift-knative.github.io/docs/docs/latest/serverless-logic/about.html)
* [SonataFlow Guides](https://kiegroup.github.io/kogito-docs/serverlessworkflow/latest/index.html)

## Running F05EB00E.D9D7.46B1.BC27.136EB02E22E1 in Quarkus dev mode
You can run your application in dev mode that enables live coding using:

```shell script
mvn compile quarkus:dev
```

## Testing with curl
First, validate the workflows exposed by the application:
```shell script
curl -v -H "Content-Type: application/json" http://localhost:8080/management/processes
```
(F05EB00E.D9D7.46B1.BC27.136EB02E22E1 should be included in the returned array)

Then, assuming that you stored in [input.json](./input.json) the input parameters (if any) following the input schema specifications at
[F05EB00E.D9D7.46B1.BC27.136EB02E22E1-schema.json](./src/main/resources/schemas/F05EB00E.D9D7.46B1.BC27.136EB02E22E1-schema.json ), run the following to create an
instance of the F05EB00E.D9D7.46B1.BC27.136EB02E22E1 workflow:
```shell script
curl -v -X POST -H "Content-Type: application/json" http://localhost:8080/F05EB00E.D9D7.46B1.BC27.136EB02E22E1 -d@input.json
```

# Dev UI Tools
Use the `Serverless Workflow Tools` to manage and monitor the published workflows:
```
http://localhost:8080/q/dev-v1/org.kie.kogito.kogito-quarkus-serverless-workflow-devui/workflowInstances
```

Use the `Data Index GraphQL UI` to query the state of the [Data Index service](https://sonataflow.org/serverlessworkflow/main/data-index/data-index-core-concepts.html):
```
http://localhost:8080/q/dev-v1/org.kie.kogito.kogito-addons-quarkus-data-index-inmemory/dataindex
```
