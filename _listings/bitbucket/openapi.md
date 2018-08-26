---
swagger: "2.0"
x-collection-name: Bitbucket
x-complete: 1
info:
  title: Bitbucket
  description: code-against-the-bitbucket-api-to-automate-simple-tasks-embed-bitbucket-data-into-your-own-site-build-mobile-or-desktop-apps-or-even-add-custom-ui-addons-into-bitbucket-itself-using-the-connect-framework-
  termsOfService: https://www.atlassian.com/legal/customer-agreement
  contact:
    name: Bitbucket Support
    url: https://support.atlassian.com/bitbucket
    email: support@bitbucket.org
  version: 1.0.0
host: api.bitbucket.org
basePath: /2.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /repositories/{username}/{repo_slug}/issues/{issue_id}/attachments/{path}:
    delete:
      summary: Delete Repositories Username Repo Slug Issues Issue  Attachments Path
      description: Delete repositories username repo slug issues issue  attachments
        path
      operationId: deleteRepositoriesUsernameRepoSlugIssuesIssueAttachmentsPath
      x-api-path-slug: repositoriesusernamerepo-slugissuesissue-idattachmentspath-delete
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Issues
      - Issue
      - ""
      - Attachments
      - Path
    get:
      summary: Get Repositories Username Repo Slug Issues Issue  Attachments Path
      description: |-
        Returns the contents of the specified file attachment.

        Note that this endpoint does not return a JSON response, but instead
        returns a redirect pointing to the actual file that in turn will return
        the raw contents.

        The redirect URL contains a one-time token that has a limited lifetime.
        As a result, the link should not be persisted, stored, or shared.
      operationId: getRepositoriesUsernameRepoSlugIssuesIssueAttachmentsPath
      x-api-path-slug: repositoriesusernamerepo-slugissuesissue-idattachmentspath-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Issues
      - Issue
      - ""
      - Attachments
      - Path
    parameters:
      summary: Parameters Repositories Username Repo Slug Issues Issue  Attachments
        Path
      description: Parameters repositories username repo slug issues issue  attachments
        path
      operationId: parametersRepositoriesUsernameRepoSlugIssuesIssueAttachmentsPath
      x-api-path-slug: repositoriesusernamerepo-slugissuesissue-idattachmentspath-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Issues
      - Issue
      - ""
      - Attachments
      - Path
  /repositories/{username}/{repo_slug}/src/{node}/{path}:
    get:
      summary: Get Repositories Username Repo Slug Src Node Path
      description: Get repositories username repo slug src node path
      operationId: getRepositoriesUsernameRepoSlugSrcNodePath
      x-api-path-slug: repositoriesusernamerepo-slugsrcnodepath-get
      parameters:
      - in: query
        name: format
        description: Instead of returning the files contents, return the (json) meta
          data for it
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Src
      - Node
      - Path
    parameters:
      summary: Parameters Repositories Username Repo Slug Src Node Path
      description: Parameters repositories username repo slug src node path
      operationId: parametersRepositoriesUsernameRepoSlugSrcNodePath
      x-api-path-slug: repositoriesusernamerepo-slugsrcnodepath-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Src
      - Node
      - Path
  /snippets/{username}/{encoded_id}/{node_id}/files/{path}:
    get:
      summary: Get Snippets Username Encoded  Node  Files Path
      description: |-
        Retrieves the raw contents of a specific file in the snippet. The
        `Content-Disposition` header will be "attachment" to avoid issues with
        malevolent executable files.

        The file's mime type is derived from its filename and returned in the
        `Content-Type` header.

        Note that for text files, no character encoding is included as part of
        the content type.
      operationId: getSnippetsUsernameEncodedNodeFilesPath
      x-api-path-slug: snippetsusernameencoded-idnode-idfilespath-get
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Node
      - ""
      - Files
      - Path
    parameters:
      summary: Parameters Snippets Username Encoded  Node  Files Path
      description: Parameters snippets username encoded  node  files path
      operationId: parametersSnippetsUsernameEncodedNodeFilesPath
      x-api-path-slug: snippetsusernameencoded-idnode-idfilespath-parameters
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Node
      - ""
      - Files
      - Path
---