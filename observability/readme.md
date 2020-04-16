# Observability

Building observable systems enables development teams at CSE to measure how well the application is behaving.

## Goals

1. Provide holistic view on the health of the application.
2. Help measure business performance for the customer.
3. Measure operational performance of the system.
4. Identify and diagnose failures to get to the problem fast.

## Sections

- [Observability](#observability)
  - [Goals](#goals)
  - [Sections](#sections)
  - [Pillars of Observability](#pillars-of-observability)
  - [Recommended Practices](#recommended-practices)
  - [Pitfalls to avoid](#pitfalls-to-avoid)
    - [Collection](#collection)
      - [1. Agent:](#1-agent)
      - [2. SDK:](#2-sdk)
      - [3. SDK-Agent:](#3-sdk-agent)
  - [Recipes](#recipes)

## Pillars of Observability

1. [Logging](pillars/logging.md)
2. [Tracing](pillars/tracing.md)
3. [Metrics](pillars/metrics.md)

## Recommended Practices

1. **Correlation Id**: Include unique identifier at the start of the interaction to tie down aggregated data from various system components and provide a holistic view. Read more guidelines about using [correlation id](correlation-id.md).
2. Ensure health of the services are **monitored** and provide insights into system's performance and behavior.
3. **Faults, crashes, and failures** are logged as discrete events. This helps engineers identify problem area(s) during failures.
4. Ensure logging configuration (eg: setting logging to "verbose") can be controlled without code changes.
5. Ensure that **metrics** around latency and duration are collected and can be aggregated.
6. Start small and add where there is customer impact.

### Collecting data with the correct data type

Metrics and log data serve complimentary but different purposes when monitoring production systems. [Read more](log-vs-metric.md) about this in a breakdown of the two data types.

## Pitfalls to avoid

Read more [here](pitfalls.md) to understand what to watch out for while designing and building an observable system.

## Recipes

1. Application Insights/ASP.NET - [Github Repo](https://github.com/Azure-Samples/application-insights-aspnet-sample-opentelemetry), [Article](https://devblogs.microsoft.com/aspnet/observability-asp-net-core-apps/).

2. [On-premise Application Insights](https://github.com/c-w/appinsights-on-premises) - A service that is compatiable with Azure App Insights, but stores the data in an in-house database.
