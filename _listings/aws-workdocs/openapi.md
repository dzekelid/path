---
swagger: "2.0"
x-collection-name: AWS WorkDocs
x-complete: 1
info:
  title: AWS WorkDocs API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=GetDocumentPath:
    get:
      summary: Get Document Path
      description: Retrieves the path information (the hierarchy from the root folder)
        for the requested document.
      operationId: getDocumentPath
      x-api-path-slug: actiongetdocumentpath-get
      parameters:
      - in: query
        name: DocumentId
        description: The ID of the document
        type: string
      - in: query
        name: Fields
        description: A comma-separated list of values
        type: string
      - in: query
        name: Limit
        description: The maximum number of levels in the hierarchy to return
        type: string
      responses:
        200:
          description: OK
      tags:
      - Documents
  /?Action=GetFolderPath:
    get:
      summary: Get Folder Path
      description: Retrieves the path information (the hierarchy from the root folder)
        for the specified folder.
      operationId: getFolderPath
      x-api-path-slug: actiongetfolderpath-get
      parameters:
      - in: query
        name: Fields
        description: A comma-separated list of values
        type: string
      - in: query
        name: FolderId
        description: The ID of the folder
        type: string
      - in: query
        name: Limit
        description: The maximum number of levels in the hierarchy to return
        type: string
      responses:
        200:
          description: OK
      tags:
      - Folders
---