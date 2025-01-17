---
title: 'Observing an API'
updated: 2022-05-25
warning: false
contextual_links:
  - type: section
    name: "Prerequisites"
  - type: link
    name: "Grouping requests in Collections"
    url: "/docs/sending-requests/intro-to-collections/"
  - type: section
    name: "Additional Resources"
  - type: subtitle
    name: "Videos"
  - type: link
    name: "Integrate with New Relic in Postman"
    url: "https://youtu.be/VwtTkHSPpMM"
  - type: subtitle
    name: "Blog Posts"
  - type: link
    name: "Integrated API Monitoring in Postman"
    url: "https://blog.postman.com/integrated-api-monitoring-in-postman/"
  - type: link
    name: "Monitor APIs with Postman and New Relic"
    url: "https://blog.postman.com/monitor-apis-with-postman-and-new-relic/"
  - type: section
    name: "Next Steps"
  - type: link
    name: "Managing APIs"
    url: "/docs/designing-and-developing-your-api/managing-apis/"
---

You can use Postman Monitors to track functionality and end-to-end performance of your APIs and response time. You can also inspect New Relic metrics for your API, and access relevant New Relic dashboards and deployments within Postman.

* [Linking collection-based monitors](#linking-collection-based-monitors)
* [Linking uptime monitors](#linking-uptime-monitors)
* [Connecting to monitor integrations](#connecting-to-monitor-integrations)
* [Viewing New Relic APM metrics](#viewing-new-relic-apm-metrics)

## Linking collection-based monitors

You can link [collection-based monitors](/docs/monitoring-your-api/setting-up-monitor/) in your current workspace to an API version. This enables you to check an API's performance and response times at scheduled intervals. From an API version's **Monitoring** tab, you can [create a new monitor](#creating-a-new-monitor) or [add an existing monitor](#adding-an-existing-monitor).

<img alt="API monitor integrations" src="https://assets.postman.com/postman-docs/api-builder-api-monitor-v9-19.jpg">

### Creating a new monitor

On the API version **Monitoring** tab, next to **Collection-based Monitors**, select **Add Monitor** and choose **Create new monitor**.

You can choose between generating a collection from your API schema, using an existing collection, or creating a new collection:

* **Generate a collection from a schema.**
    1. Specify a name for the collection.
    1. Configure how the collection will be generated by selecting **Show advanced settings**.
    1. Select **Generate collection and continue**.
* **Use an existing collection.**
    1. Choose an existing collection in the dropdown list.
    1. Select **Select Collection and Continue**.
* **Create a new collection.**
    1. Add the requests you plan to monitor, specifying the method and URL, along with the status code and response time you want to check.
    1. Select **Create Collection and Continue**.

Next, configure the new monitor. For details, see [Configuring a collection-based monitor](/docs/monitoring-your-api/setting-up-monitor/#configuring-a-collection-based-monitor).

### Adding an existing monitor

To add an existing monitor to your API:

1. On the API version **Monitoring** tab, next to **Collection-based Monitors**, select **Add Monitor** and choose **Add existing monitor**.
1. Select a collection-based monitor from the list and select **Add Monitor**. (The list shows monitors available in your current workspace.)

For more about creating a monitor, see [Setting up a collection-based monitor](/docs/monitoring-your-api/setting-up-monitor/).

## Linking uptime monitors

You can link [uptime monitors](/docs/monitoring-your-api/uptime-monitors/) in your current workspace to an API version. Uptime monitors (open beta) continuously check the availability of a single API endpoint, website, or other URL. After linking an uptime monitor, you can view the current status and key statistics for the last three hours, such as availability, the number of downtime incidents, and average response time.

To add an existing uptime monitor to your API:

1. On the API version **Monitoring** tab, next to **Uptime Monitors**, select **Add Monitor** and choose **Add existing monitor**.
1. Select an uptime monitor from the list and select **Add Monitor**. (The list shows monitors available in your current workspace.)

For more about creating an uptime monitor, see [Monitoring API uptime](/docs/monitoring-your-api/uptime-monitors/).

<img alt="API monitor integrations" src="https://assets.postman.com/postman-docs/api-builder-uptime-monitor-v9-19.jpg">

## Connecting to monitor integrations

Postman integrations enable you to send the results of collection-based monitors to a variety of applications and channels, such as Slack, Microsoft Teams, Datadog, or Splunk. You can also send monitor results to a custom webhook to integrate Postman monitors with your specific workflow.

The **Monitoring** tab in the API Builder provides one place to manage all your API's integrations for collection-based monitors. You can set up a new integration, track results, and view your configured monitor integrations.

> You can also set up a Slack integration for uptime monitors. Learn more about [integrating uptime monitors and Slack](/docs/monitoring-your-api/uptime-monitors/#getting-notified-about-downtime).

<img alt="API monitor integrations" src="https://assets.postman.com/postman-docs/observe-api-integrations-v9-19.jpg">

### Adding a monitor integration

Connect an API version to one or more monitoring integrations to send collection-based monitor results to other applications that are part of your API development workflow. When you add a monitor integration, the monitor is automatically [linked to the API version](#linking-monitors).

1. If you haven't done so already, [create the collection-based monitor](/docs/monitoring-your-api/intro-monitors/) you want to connect to your API.
1. Open an API version and select the **Monitoring** tab.
1. Under **Connect Postman to your monitoring workflows**, select a monitor integration.
1. Enter a **Nickname** for the integration and choose a monitor. Postman will send the results of this monitor to the application you're integrating with.
1. Finish entering the requested information. This information varies depending on the application you're integrating with, and typically includes an API key. For more help with a specific application, see [Integrating with Postman](/docs/integrations/intro-integrations/) and select [Available integrations](/docs/integrations/available-integrations/apimatic/) in the left navigation pane.
1. Select **Add integration**.

> You can configure multiple integrations for a collection-based monitor, or even have more than one instance of the same integration. For example, you can configure two Slack integrations for a monitor that send the monitor's results to two different Slack channels.

### Working with monitor integrations

Once you've added a monitor integration to an API version, you can take the following actions on the **Monitoring** tab:

* Select a monitor's name to open its dashboard in a new tab.
* Select **Validate** next to a monitor to validate it against the API schema (OpenAPI 3.0 schemas). If validation isn't successful, select **Issues found** and then select **Review issues**. Learn more about [validating APIs](/docs/designing-and-developing-your-api/validating-elements-against-schema/).
* Hover over a bar in the graph to view metrics for a monitor run.

  <img alt="API monitor results" src="https://assets.postman.com/postman-docs/observe-api-integrations-results-v9-10.jpg" width="332px">

* Hover over the application icon for an integration to view details. Select the **Edit** icon <img alt="Edit icon" src="https://assets.postman.com/postman-docs/documentation-edit-icon-v8-10.jpg#icon" width="18px"> to edit the integration, or select the **Delete** icon <img alt="Delete icon" src="https://assets.postman.com/postman-docs/icon-delete-v9.jpg#icon" width="12px"> to delete the integration.

  <img alt="Edit an API monitor" src="https://assets.postman.com/postman-docs/observe-api-integrations-modify-v9-10.jpg" width="332px">

* Hover over a monitor and select **Run** to immediately run the monitor.
* Hover over a monitor and select the remove icon <img alt="Remove icon" src="https://assets.postman.com/postman-docs/icon-remove-api-element-v9.jpg#icon" width="16px"> to remove the monitor from the API version. (The monitor and its associated integrations aren't deleted.)

## Viewing New Relic APM metrics

New Relic is an application performance management (APM) solution to monitor real-time and trending data for your processes or web apps. The API Builder has a New Relic integration that enables you to access New Relic APM metrics from directly within Postman.

With this integration, each version of your API in Postman can be linked to multiple services from New Relic. Each service can correspond to a running instance of the API, such as beta, prod1, and prod2. You can also optionally link multiple dashboards from New Relic to your API.

> **You can also send Postman monitor results to New Relic.** Note that sending monitor results to New Relic is a separate integration from viewing APM metrics and uses a different New Relic API key. The integration in the API Builder has two tabs to cover both integrations. Learn more about [configuring a Postman monitor integration with New Relic](/docs/integrations/available-integrations/new-relic/).

### Connecting to New Relic APM

Before beginning, you must set up APM services for each deployment of your API. See [the New Relic APM documentation](https://docs.newrelic.com/docs/apm/) for more details.

To connect an API to New Relic APM:

1. Open an API version and select the **Monitoring** tab.
1. Under **Connect Postman to your monitoring workflows**, select **New Relic APM**.
1. On the **Monitor API performance** tab:
    * Enter a New Relic User API Key.

        > There are multiple types of API keys in New Relic. Make sure to use a **User** key for connecting an API to New Relic. For more information on API keys in New Relic, read the [New Relic API keys documentation](https://docs.newrelic.com/docs/apis/intro-apis/new-relic-api-keys/).
1. In **Services** select one or more of your New Relic APM services.
1. Optionally, in **Link dashboard**, select one or more of your New Relic Dashboards.
1. Select your New Relic region.
1. Select **Connect**.

> You can also optionally select **Post monitoring results** and configure an integration to send your Postman monitor run metrics to New Relic. This uses a different New Relic API key. Learn more about [configuring a Postman monitor integration with New Relic](/docs/integrations/available-integrations/new-relic/).

### Using the APM dashboard

Once your New Relic connection is established, the **Monitoring** tab will show a table of your services, along with their latency, error rate, apdex (ratio of successful to total requests), and health status.

Health status is based on violations of alert conditions in New Relic, as shown in the table below. For more information, read the New Relic documentation for [viewing alert violations](https://docs.newrelic.com/docs/alerts-applied-intelligence/new-relic-alerts/alert-violations/view-alert-violations-our-products/).

| Status | Description |
| ----------- | ----------- |
| Healthy | No entity has violations and there are no alerts |
| Warning | An entity has a warning violation in progress |
| Critical | An entity has a critical violation in progress |
| Not configured | No entity is configured for alerting |

You can also select **Dashboard Quicklinks** to choose a link to any of your configured New Relic dashboards. The links will open the dashboard page in New Relic in a new browser window.

![](https://assets.postman.com/postman-docs/api-builder-nr-services.jpg)

Select the name of a service to open a new tab in Postman containing an APM dashboard. The dashboard is updated with:

* Graphs for web transaction time, throughput, error rate, and apdex score. Select a point on a graph to show an exact value for that time.
* Tables of violation Events, slowest transactions by time, and deployments.
* Status if the service is still healthy.

At the top of the dashboard tab, you can:

* Choose another service to view.
* Select **View on New Relic** to open the APM summary in New Relic in a new browser window.
* Choose a time range for the metrics shown.
* Refresh the data in the tab.

    <img src="https://assets.postman.com/postman-docs/api-builder-apm-page.jpg" alt="New Relic APM" width="350px"/>

To reconfigure the connection to New Relic, select the more actions icon <img alt="More actions icon" src="https://assets.postman.com/postman-docs/icon-more-actions-v9.jpg#icon" width="16px"> and choose **Edit integration**. You can then change the nickname, API key, services, dashboards, or region. You can also choose **Delete integration** to remove the connection.
