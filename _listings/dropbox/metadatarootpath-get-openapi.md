---
swagger: "2.0"
x-collection-name: Dropbox
x-complete: 0
info:
  title: Dropbox Core Retrieves file and folder metadata.
  description: |-
    Retrieves file and folder metadata.

    **Note:** `modified`, `rev`, and `revision` aren't returned in the metadata for the root/top-level path.
  termsOfService: https://www.dropbox.com/developers/reference/tos
  contact:
    name: Dropbox
    url: https://www.dropbox.com/developers
  version: 1.0.0
host: api.dropbox.com
basePath: /1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /metadata/{root}/{path}:
    get:
      summary: Retrieves file and folder metadata.
      description: |-
        Retrieves file and folder metadata.

        **Note:** `modified`, `rev`, and `revision` aren't returned in the metadata for the root/top-level path.
      operationId: retrieves-file-and-folder-metadatanote-modified-rev-and-revision-arent-returned-in-the-metadata-for-
      x-api-path-slug: metadatarootpath-get
      parameters:
      - in: query
        name: file_limit
        description: Default is 10,000 (max is 25,000)
      - in: query
        name: hash
        description: Each call to `/metadata` on a folder will return a `hash` field,
          generated by hashing all of the metadatacontained in that response
      - in: query
        name: include_deleted
        description: Only applicable when `list` is set
      - in: query
        name: include_media_info
        description: If `true`, each file will include a `photo_info` dictionary for
          photos and a `video_info` dictionaryfor videos with additional media info
      - in: query
        name: include_membership
        description: If `true`, metadata for a shared folder will include a list of
          members and a list of groups
      - in: query
        name: list
        description: The strings `true` and `false` are valid values
      - in: query
        name: locale
        description: The metadata returned will have its `size` field translated based
          on the given `locale`
      - in: path
        name: path
        description: The path to the file or folder
      - in: query
        name: rev
        description: If you include a particular revision number, then only the metadata
          for that revision will be returned
      - in: path
        name: root
        description: 'Root folder: `auto` - automatically determines the appropriate
          root folder using your apps permissionlevel (recommended); `sandbox` - the
          codename for app folder level; `dropbox` - full dropbox access'
      responses:
        200:
          description: OK
      tags:
      - Storage
      - Documents
      - Metadata
      - Root
      - Path
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---