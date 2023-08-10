# Helm Charts Quick Guide

# What is Helm?

Helm stands as an open source package manager designed for Kubernetes, enabling the provisioning, sharing, and utilization of software developed for the Kubernetes environment.  What is a Chart?

A `Chart` stands as a Helm package encompassing all the essential resource explanations essential for executing an application, tool, or service within a Kubernetes cluster.

## How to create a Chart:

helm create <name_of_chart>
`Generates a directory for charts, accompanied by the standard files and folders utilized within a chart.`

## Chart directory guide.

* #### templates/ directory:

The `templates/` directory is for template files. 

* #### values.yaml file:
  
This file contains the default values for a chart.

* #### Chart.yaml file:
  
The `Chart.yaml` file contains a description of the chart.

## Chart.yaml file guide:

```
apiVersion: The chart API version (required)
name: The name of the chart (required)
description: A single-sentence description of this project (optional)
type: The type of the chart (optional)
version: A SemVer 2 version (required)
appVersion: The version of the app that this contains (optional). Needn't be SemVer. Quotes recommended.
maintainers: # (optional)
  - name: The maintainers name (required for each maintainer)
    email: The maintainers email (optional for each maintainer)
```

* #### charts/ directory:
  
The `charts/` directory may contain other charts (which we call subcharts).
