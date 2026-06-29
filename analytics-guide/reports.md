---
description: Analytics is a page for viewing reports and data analysis results. Users can view charts, reports, and related analytical content to quickly understand data status and improve browsing and interpretation efficiency.
---

# Reports

## Introduction

Reports provide usage and operational analytics for AI Studio, helping administrators track Token usage, Quota, task execution, and feature utilization across the platform. Users can view data related to Session, Memory, Workflow, RAG, Speech, and more through visual dashboards, serving as a reference for cost analysis, usage tracking, and operational management.

This page integrates reporting and data visualization tools. Users can view existing Dashboards, Charts, and Datasets based on their permissions.

<figure><img src="../.gitbook/assets/image (401).png" alt=""><figcaption></figcaption></figure>

## Dashboard

**Dashboard** is used to centrally display created analytics dashboards. Each Dashboard contains one or more charts for monitoring data on specific topics.

Common Dashboard topics may include:

* Agent usage status
* Token usage and costs
* User activity analysis
* Knowledge Base and Agent relationships
* Permissions and access status
* Task execution and anomaly monitoring

In the Dashboard list, users can view the name, status, owner, and last modified time. Clicking a Dashboard name opens that Dashboard to view detailed chart content.

## Chart

**Chart** is used to manage or create report charts. When creating a chart, users must first select a dataset, then choose a chart type.

The system supports multiple chart types, such as:

* Area Chart
* Bar Chart
* Big Number
* Line Chart
* Pie Chart
* Table
* Heatmap
* Pivot Table
* Scatter Plot
* Treemap

Different chart types are suited for different data. For example, use a Line Chart for trend data, a Pie Chart for proportional data, a Table for detailed records, and a Big Number for key metrics.

The ability to create Charts is typically provided to users with report management permissions. General users can view existing charts and Dashboards based on their permissions.

## Dataset

**Dataset** displays the data sets available for creating charts and Dashboards. A Dataset is the data source for report analysis; charts are generated based on the fields and data in the selected Dataset.

In the Dataset list, users can view the dataset name, type, database, schema, owner, and last modified time.

## Notes

The Dashboards, Charts, and Datasets visible in Reports vary based on user permissions. If a specific report or dataset is not visible, please confirm whether you have the corresponding view or management permissions.

This page is primarily for data viewing and analysis. To modify a Dashboard, Chart, or Dataset, confirm that you have report management permissions and configure accordingly.
