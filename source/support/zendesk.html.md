---
title: Zendesk guide
---

# Zendesk guide

Teaching the wider Zendesk interface is out-of-scope of this guide, but it records key things in our usage.

We use the [GOV.UK Zendesk](https://govuk.Zendesk.com/agent/filters) for managing support tickets and some automated notifications.

We have two sorts of tickets: ordinary support dealt with in-hours, and P1 incidents dealt with out-of-hours. We have an extra view for ordinary tickets requiring attention from the product people.

There are multiple inputs for ordinary support tickets: forms on the product page, emails to the `gov-uk-paas-support@digital.cabinet-office.gov.uk` address, automated CVE alerts, etc.

To bring tickets to the attention of PaaS product people, add the `paas_product_support` tag.

A few people in the team have edit permissions over our own views, but for most changes we need to talk to the GDS support team within TechOps. Open a Zendesk ticket assigned to `2nd/3rd Line--Zendesk Administration`.

Email notifications of incoming tickets are administered manually. This needs doing when someone is added or removed from Zendesk. Contact the support team.

## Routing

The in-hours email address `gov-uk-paas-support@digital.cabinet-office.gov.uk` is given in numerous places, for instance our [Support](https://admin.london.cloud.service.gov.uk/support) page. The out-of-hours email address is deliberately not written down in public, to avoid spam waking people up at night.

Both email addresses are Google Groups. Originally we used Gmail Aliases but they did not support prepending to email subjects for Zendesk. These groups forward emails elsewhere and are not intended for use by themselves. Their spam protection is disabled to avoid emails being silently discarded.

The in-hours email address prepends `[PaaS Support]` to email subjects, and forwards it to a Zendesk email address. The out-of-hours email address prepends `[PaaS Emergency Support]` and also forwards to a PagerDuty email address.

## Tagging

In hours support is responsible for tagging incoming tickets to enable analysis.

We use the following tags to categorise support tickets:

<div style="height:1px;font-size:1px;">&nbsp;</div>

|Name| Tag| Description |
|:---|:---|:---|
|# Activity update|paas_activity_update|The tenant is providing the GOV.UK PaaS team with information about their activity, this could be load testing, penetration testing, moving the service to live|
|# Account lifecycle|paas_account_lifecycle|Topic category for support requests relating to creating, maintaining and deleting organisations|
|# Backing service|paas_backing_service|The tenant has a question about backing services: mysql, postgres, redis, elasticsearch, influxdb, cdn, autoscaling|
|# Bug|paas_bug|The tenant has encountered a bug, error or fault in GOV.UK PaaS that we need to fix.|
|# Buildpacks|paas_buildpacks|The tenant has a question about buildpacks|
|# CC|paas_cc|Non actionable items, information from upstream and others|
|# Consultancy|paas_consultancy|The tenant needs advice and expertise from a member of the GOV.UK PaaS team in the form of a meeting or phone call to determine suitability, billing, pricing, roadmap|
|# Deployment|paas_deployment|The tenant is having issues deploying an application to the platform|
|# Feature request|paas_feature_request|The tenant needs or wants a new feature that GOV.UK PaaS does not offer|
|# Incident|paas_incident_report|The tenant is reporting an incident|
|# Logging/Monitoring/Alerting|paas_logging_monitoring_alerting|The tenant has a query, request or problem related to monitoring, metrics, logs |
|# Misc|paas_misc|The ticket does not fit into any of the existing tags|
|# Missing information|paas_missing_information |The tenant is unable to find the information they're looking for |
|# Platform monitoring|paas_monitoring|Informational items that come from our platform monitoring systems (Pingdom, Cronitor, PagerDuty)|
|# Org billable|paas_org_billable|The tenant has a query about billing or wants to go move to a billable plan|
|# Org demise|paas_org_demise|An organisation is to be demised|
|# Org quota|paas_org_quota|The tenant is requesting to increase their usage quota|
|# Org trial|paas_org_trial|A prospective tenant is requesting a trial account to evaluate the use of the platform|
|# Out of hours|paas_outofhours|Out of hours support|
|# Action|paas_paas_action|The tenant needs the GOV.UK PaaS team to perform an action for them|
|# Platform tests|paas_platform_tests|Automated messages from smoketest pipeline|
|# Question|paas_question|The tenant needs more information about GOV.UK PaaS|
|# Routing|paas_routing|The tenant is having issues with routing|
|# Security|paas_security|Topic category for security-related questions. The tenant has a question or problem related to security or information assurance|
|# Spam|paas_spam|Unsolicited off topic tickets|
|# Technology|paas_technology|Topic category for tech-support requests|
|# Tenant action|paas_tenant_action|The tenant needs to perform an action for the GOV.UK PaaS team|
|# Test|paas_test|test tickets generated by user testing that should be ignored|
|# Troubleshooting|paas_troubleshooting|The tenant needs help to identify and resolve an issue they are experiencing|
|# Upstream|paas_upstream|Actionable items that come from our upstream providers (AWS, Aiven, Cloud Foundry Foundation) leaked keys, ec2 abuse, phishing websites, deprecation notices, cve notifications from the Cloud Foundry Foundation|
|# User account|paas_user_account|The tenant needs help to do something with their account. For example, resetting a password, adding or removing a user|

<div style="height:1px;font-size:1px;">&nbsp;</div>
