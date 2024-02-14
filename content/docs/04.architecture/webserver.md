---
title: Webserver
icon: /docs/icons/architecture.svg
---

Webserver serves the APIs and the User Interface (UI).

The **Webserver** offers two main modules in the same component:
- **API**: All the [APIs](../11.api-reference/index.md) that allow triggering executions for any system, and interacting with Kestra.
- **UI**: The [User Interface](../01.getting-started/14.ui.md) (UI) is also served by the Webserver.

The Webserver interacts mostly with the Repository to deliver a rich API/UI. It also interacts with the Queue to trigger new executions, follow executions in real-time, etc.


::alert{type="info"}
Each server component (other than the Scheduler) can continue to work as long as the Queue is up and running. The Repository is only used to help provide our rich Webserver UI, and even if the Repository is down, workloads can continue to process on Kestra.
::