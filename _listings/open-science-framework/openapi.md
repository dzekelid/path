---
swagger: "2.0"
x-collection-name: Open Science Framework
x-complete: 1
info:
  title: Open Science Framework
  description: osf-provides-free-and-open-source-project-management-support-for-researchers-across-the-entire-research-lifecycle--as-a-collaboration-tool-osf-helps-researchers-work-on-projects-privately-with-a-limited-number-of-collaborators-and-make-parts-of-their-projects-public-or-make-all-the-project-publicly-accessible-for-broader-dissemination--as-a-workflow-system-osf-enables-connections-to-the-many-services-researchers-already-use-to-streamline-their-process-and-increase-efficiency--as-a-flexible-repository-it-can-store-and-archive-research-data-protocols-and-materials--
  contact:
    name: OSF
    url: https://osf.io/support
    email: support@osf.io
  version: "2.0"
host: test-api.osf.io
basePath: /v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /nodes/{node_id}/files/{provider}/{path}/:
    get:
      summary: Retrieve a file
      description: |-
        Retrieves the details of a file attached to given node (project or component) for the given storage provider.
        ####Returns
        Returns a JSON object with a `data` key containing the representation of the requested file object, if the request is successful.

        If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
      operationId: nodes_files_read
      x-api-path-slug: nodesnode-idfilesproviderpath-get
      parameters:
      - in: path
        name: node_id
        description: The unique identifier of the node
      - in: path
        name: path
        description: The unique identifier of the file path
      - in: path
        name: provider
        description: The unique identifier of the storage provider
      responses:
        200:
          description: OK
      tags:
      - Nodes
      - Node
      - Files
      - Provider
      - Path
  /registrations/{registration_id}/files/{provider}/{path}/:
    get:
      summary: Retrieve a file
      description: |-
        Retrieves the details of a registration file for the given storage provider.
        ####Returns
        Returns a JSON object with a `data` key containing the representation of the requested registration file object, if the request is successful.

        If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
      operationId: registrations_files_read
      x-api-path-slug: registrationsregistration-idfilesproviderpath-get
      parameters:
      - in: path
        name: path
        description: The unique identifier of the file path
      - in: path
        name: provider
        description: The unique identifier of the storage provider
      - in: path
        name: registration_id
        description: The unique identifier of the registration
      responses:
        200:
          description: OK
      tags:
      - Registrations
      - Registration
      - Files
      - Provider
      - Path
---