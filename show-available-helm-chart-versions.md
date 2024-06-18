To list all available versions of a Helm chart, you can use the Helm command-line tool with the `search repo` command. This command searches the Helm repositories for the specified chart and displays available versions.

### Prerequisites

1. **Helm CLI**: Ensure you have Helm installed. You can install Helm by following the instructions on the [official Helm website](https://helm.sh/docs/intro/install/).

2. **Configured Helm Repositories**: Make sure your Helm repositories are configured. For example, you should have the default Helm repository (`stable`), or any other repositories where the charts are hosted.

### Steps to List All Versions of a Helm Chart

1. **Add Helm Repositories** (if not already added):

    ```sh
    helm repo add stable https://charts.helm.sh/stable
    helm repo add bitnami https://charts.bitnami.com/bitnami
    helm repo update
    ```

    Replace `stable` and `bitnami` with the appropriate repository if your chart is hosted elsewhere.

2. **Search for the Chart**:

    To list all versions of a specific chart (e.g., `kafka` from the `bitnami` repository), use the following command:

    ```sh
    helm search repo bitnami/kafka --versions
    ```

    This command will display all available versions of the `kafka` chart from the `bitnami` repository.

### Example

Here's a complete example to list all versions of the `kafka` chart from the `bitnami` repository:

1. **Add the Bitnami Repository** (if not already added):

    ```sh
    helm repo add bitnami https://charts.bitnami.com/bitnami
    helm repo update
    ```

2. **List All Versions of the Kafka Chart**:

    ```sh
    helm search repo bitnami/kafka --versions
    ```

    The output will look something like this:

    ```plaintext
    NAME            CHART VERSION   APP VERSION DESCRIPTION
    bitnami/kafka   14.4.1          2.8.0       Apache Kafka is a distributed streaming platform.
    bitnami/kafka   14.4.0          2.8.0       Apache Kafka is a distributed streaming platform.
    bitnami/kafka   14.3.3          2.8.0       Apache Kafka is a distributed streaming platform.
    ...
    ```

### Notes

- The `helm search repo` command with the `--versions` flag will show all available versions of the specified chart.
- Make sure your Helm repositories are up-to-date by running `helm repo update` before searching for charts.
- You can specify any repository and chart name to list available versions.

Using this approach, you can list all versions of any Helm chart available in your configured repositories.
