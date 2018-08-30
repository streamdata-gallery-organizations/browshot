---
swagger: "2.0"
x-collection-name: Browshot.com
x-complete: 0
info:
  title: Browshot Get the batch status
  description: Get the status of a batch requested through the API or through the
    dashboard.
  termsOfService: https://browshot.com/terms
  contact:
    name: API Support
    url: https://browshot.com/contact
    email: support@browshot.com
  version: 1.17.0
host: api.browshot.com
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /account/info:
    get:
      summary: Get information about your account
      description: Get information about your account.
      operationId: GetAccountInfo
      x-api-path-slug: accountinfo-get
      parameters:
      - in: query
        name: details
        description: level of information returned
      responses:
        200:
          description: OK
      tags:
      - Account
      - Info
  /batch/ceate:
    post:
      summary: Requests thousands of screenshtos at once
      description: Get hundreds or thousands of screenshots from a text file. You
        can use this API call or the dashboard. Unlike the other API calls, you must
        issue a POST request with the Content-Type "multipart/form-data" in order
        to upload the text file. The text file must contain the list of URLs to request,
        1 URL per line. Failed screenshots will be tried up to 3 times before giving
        up.
      operationId: CreateBatch
      x-api-path-slug: batchceate-post
      parameters:
      - in: formData
        name: cookie
        description: set a cookie for the URL requested (see Custom POST Data, Referer
          and Cookie) Cookies should be separated by a ; - paid screenshots only
      - in: formData
        name: delay
        description: number of seconds to wait after the page has loaded
      - in: formData
        name: details
        description: level of information available with screenshot/info
      - in: formData
        name: file
        description: text file to use
      - in: formData
        name: flash_delay
        description: number of seconds to wait after the page has loaded if Flash
          elements are present
      - in: formData
        name: format
        description: image as PNG or JPEG
      - in: formData
        name: headers
        description: any custom HTTP headers
      - in: formData
        name: height
        description: thumbnail height
      - in: query
        name: hosting
        description: hosting option - s3 or browshot
      - in: query
        name: hosting_bucket
        description: S3 bucket to upload the screenshot or thumbnail (required for
          S3)
      - in: query
        name: hosting_file
        description: file name to use (for S3 only)
      - in: query
        name: hosting_headers
        description: list of headers to add to the S3 object (for S3 only)
      - in: query
        name: hosting_height
        description: maximum height of the thumbnail to host
      - in: query
        name: hosting_scale
        description: scale of the thumbnail to host
      - in: query
        name: hosting_width
        description: maximum height of the thumbnail to host
      - in: formData
        name: html
        description: saves the HTML of the rendered page which can be retrieved by
          the API call screenshot/html
      - in: formData
        name: instance_id
        description: instance ID to use
      - in: formData
        name: max_wait
        description: maximum number of seconds to wait before triggering the PageLoad
          event
      - in: formData
        name: name
        description: name of the batch
      - in: formData
        name: post_data
        description: send a POST requests with post_data, useful for filling out forms
          - paid screenshots only
      - in: formData
        name: priority
        description: assign priority to the screenshot (for private instances only)
      - in: formData
        name: referer
        description: use a custom referrer header - paid screenshots only
      - in: formData
        name: screen_height
        description: height of the browser window
      - in: formData
        name: screen_width
        description: width of the browser window
      - in: formData
        name: script
        description: URL of javascript file to execute after the page load event
      - in: formData
        name: size
        description: screenshots size - screen (default) or page
      - in: formData
        name: width
        description: thumbnail width
      responses:
        200:
          description: OK
      tags:
      - Batch
      - Ceate
  /batch/info:
    get:
      summary: Get the batch status
      description: Get the status of a batch requested through the API or through
        the dashboard.
      operationId: GetBatchInfo
      x-api-path-slug: batchinfo-get
      parameters:
      - in: query
        name: id
        description: batch ID
      responses:
        200:
          description: OK
      tags:
      - Batch
      - Info
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