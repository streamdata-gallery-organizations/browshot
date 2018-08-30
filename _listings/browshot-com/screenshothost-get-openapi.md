---
swagger: "2.0"
x-collection-name: Browshot.com
x-complete: 0
info:
  title: Browshot Host thumbnails on your own S3 account or on Browshot.
  description: You can host screenshots and thumbnails on your own S3 account or on
    Browshot.
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
  /browser/info:
    get:
      summary: Get information about a browser
      description: Get information about a browser.
      operationId: GetBrowserInfo
      x-api-path-slug: browserinfo-get
      parameters:
      - in: query
        name: id
        description: browser ID
      responses:
        200:
          description: OK
      tags:
      - Browser
      - Info
  /browser/list:
    get:
      summary: Get all browsers
      description: Get all browsers.
      operationId: GetBrowsersInfo
      x-api-path-slug: browserlist-get
      responses:
        200:
          description: OK
      tags:
      - Browser
      - List
  /instance/info:
    get:
      summary: Get information about an instance
      description: Get information about an instance.
      operationId: GetInstanceInfo
      x-api-path-slug: instanceinfo-get
      parameters:
      - in: query
        name: id
        description: instance ID
      responses:
        200:
          description: OK
      tags:
      - Instance
      - Info
  /instance/list:
    get:
      summary: Get all instances
      description: Get all instances.
      operationId: GetInstancesInfo
      x-api-path-slug: instancelist-get
      responses:
        200:
          description: OK
      tags:
      - Instance
      - List
  /screenshot/create:
    get:
      summary: Request a screenshot
      description: |-
        Screenshots requests to private and shared instances require a positive balance.

        *IMPORTANT*: Remember that you can only do 100 free screenshots per month. To used a premium instance, use instance_id=65 for example.
      operationId: CreateScreenshot
      x-api-path-slug: screenshotcreate-get
      parameters:
      - in: query
        name: cache
        description: use a previous screenshot (same URL, same instance) if it was
          done within  seconds
      - in: query
        name: cookie
        description: set a cookie for the URL requested (see Custom POST Data, Referer
          and Cookie) Cookies should be separated by a ; - paid screenshots only
      - in: query
        name: delay
        description: number of seconds to wait after the page has loaded
      - in: query
        name: details
        description: level of information available with screenshot/info
      - in: query
        name: flash_delay
        description: number of seconds to wait after the page has loaded if Flash
          elements are present
      - in: query
        name: headers
        description: any custom HTTP headers
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
      - in: query
        name: html
        description: saves the HTML of the rendered page which can be retrieved by
          the API call screenshot/html
      - in: query
        name: instance_id
        description: instance ID to use
      - in: query
        name: max_wait
        description: maximum number of seconds to wait before triggering the PageLoad
          event
      - in: query
        name: post_data
        description: send a POST requests with post_data, useful for filling out forms
          - paid screenshots only
      - in: query
        name: priority
        description: assign priority to the screenshot (for private instances only)
      - in: query
        name: referer
        description: use a custom referrer header - paid screenshots only
      - in: query
        name: screen_height
        description: height of the browser window
      - in: query
        name: screen_width
        description: width of the browser window
      - in: query
        name: script
        description: URL of javascript file to execute after the page load event
      - in: query
        name: shots
        description: take multiple screenshots of the same page
      - in: query
        name: shot_interval
        description: number of seconds between 2 screenshots
      - in: query
        name: size
        description: screenshot size - screen (default) or page
      - in: query
        name: url
        description: URL of the page to get a screenshot for
      responses:
        200:
          description: OK
      tags:
      - Screenshot
      - Create
  /screenshot/delete:
    get:
      summary: Delete screenshot data
      description: You can delete details of your screenshots to remove any confidential
        information.
      operationId: DeleteScreenshot
      x-api-path-slug: screenshotdelete-get
      parameters:
      - in: query
        name: data
        description: data to remove
      - in: query
        name: id
        description: screenshot ID
      responses:
        200:
          description: OK
      tags:
      - Screenshot
      - Delete
  /screenshot/host:
    get:
      summary: Host thumbnails on your own S3 account or on Browshot.
      description: You can host screenshots and thumbnails on your own S3 account
        or on Browshot.
      operationId: HostScreenshot
      x-api-path-slug: screenshothost-get
      parameters:
      - in: query
        name: bucket
        description: S3 bucket to upload the screenshot or thumbnail - required with
          hosting=s3
      - in: query
        name: file
        description: file name to use - optional, used with hosting=s3
      - in: query
        name: headers
        description: HTTP headers to add to your S3 object - optional, used with hosting=s3
      - in: query
        name: height
        description: height of the thumbnail
      - in: query
        name: hosting
        description: 'hosting option: s3 or browshot'
      - in: query
        name: id
        description: screenshot ID
      - in: query
        name: scale
        description: scale of the thumbnail
      - in: query
        name: width
        description: width of the thumbnail
      responses:
        200:
          description: OK
      tags:
      - Screenshot
      - Host
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