swagger: "2.0"
x-collection-name: Google App Engine
x-complete: 1
info:
  title: Google App Engine Admin
  description: provisions-and-manages-app-engine-applications-
  contact:
    name: Google
    url: https://google.com
  version: v1
host: appengine.googleapis.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/apps/{appsId}/services/{servicesId}/versions/{versionsId}/instances:
    get:
      summary: Get Instances
      description: 'Lists the instances of a version.Tip: To aggregate details about
        instances over time, see the Stackdriver Monitoring API (https://cloud.google.com/monitoring/api/ref_v3/rest/v3/projects.timeSeries/list).'
      operationId: appengine.apps.services.versions.instances.list
      x-api-path-slug: v1appsappsidservicesservicesidversionsversionsidinstances-get
      parameters:
      - in: path
        name: appsId
        description: Part of `parent`
      - in: query
        name: pageSize
        description: Maximum results to return per page
      - in: query
        name: pageToken
        description: Continuation token for fetching the next page of results
      - in: path
        name: servicesId
        description: Part of `parent`
      - in: path
        name: versionsId
        description: Part of `parent`
      responses:
        200:
          description: OK
      tags:
      - Instance
  /v1/apps/{appsId}/services/{servicesId}/versions/{versionsId}/instances/{instancesId}:
    delete:
      summary: Stop Instance
      description: Stops a running instance.
      operationId: appengine.apps.services.versions.instances.delete
      x-api-path-slug: v1appsappsidservicesservicesidversionsversionsidinstancesinstancesid-delete
      parameters:
      - in: path
        name: appsId
        description: Part of `name`
      - in: path
        name: instancesId
        description: Part of `name`
      - in: path
        name: servicesId
        description: Part of `name`
      - in: path
        name: versionsId
        description: Part of `name`
      responses:
        200:
          description: OK
      tags:
      - Instance
    get:
      summary: Get Instance
      description: Gets instance information.
      operationId: appengine.apps.services.versions.instances.get
      x-api-path-slug: v1appsappsidservicesservicesidversionsversionsidinstancesinstancesid-get
      parameters:
      - in: path
        name: appsId
        description: Part of `name`
      - in: path
        name: instancesId
        description: Part of `name`
      - in: path
        name: servicesId
        description: Part of `name`
      - in: path
        name: versionsId
        description: Part of `name`
      responses:
        200:
          description: OK
      tags:
      - Instance