---
name: Browshot.com
x-slug: browshot-com
description: Browshot is a service to take screenshot of web pages. Use any of our
  mobile and desktop browsers. We provide a powerful API and libraries.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/717-browshot-com.jpg
x-kinRank: "7"
x-alexaRank: "1714303"
tags: Browshot.com
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/apis.md
specificationVersion: "0.14"
apis:
- name: Browshot Get information about your account
  x-api-slug: browshot
  description: Get information about your account.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/717-browshot-com.jpg
  humanURL: http://browshot.com
  baseURL: https://api.browshot.com//api/v1//account/info
  tags: Account,Info
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/accountinfo-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/accountinfo-get-openapi.md
- name: Browshot Requests thousands of screenshtos at once
  x-api-slug: browshot
  description: Get hundreds or thousands of screenshots from a text file. You can
    use this API call or the dashboard. Unlike the other API calls, you must issue
    a POST request with the Content-Type "multipart/form-data" in order to upload
    the text file. The text file must contain the list of URLs to request, 1 URL per
    line. Failed screenshots will be tried up to 3 times before giving up.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/717-browshot-com.jpg
  humanURL: http://browshot.com
  baseURL: https://api.browshot.com//api/v1//batch/ceate
  tags: Batch,Ceate
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/batchceate-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/batchceate-post-openapi.md
- name: Browshot Get the batch status
  x-api-slug: browshot
  description: Get the status of a batch requested through the API or through the
    dashboard.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/717-browshot-com.jpg
  humanURL: http://browshot.com
  baseURL: https://api.browshot.com//api/v1//batch/info
  tags: Batch,Info
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/batchinfo-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/batchinfo-get-openapi.md
- name: Browshot Get information about a browser
  x-api-slug: browshot
  description: Get information about a browser.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/717-browshot-com.jpg
  humanURL: http://browshot.com
  baseURL: https://api.browshot.com//api/v1//browser/info
  tags: Browser,Info
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/browserinfo-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/browserinfo-get-openapi.md
- name: Browshot Get all browsers
  x-api-slug: browshot
  description: Get all browsers.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/717-browshot-com.jpg
  humanURL: http://browshot.com
  baseURL: https://api.browshot.com//api/v1//browser/list
  tags: Browser,List
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/browserlist-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/browserlist-get-openapi.md
- name: Browshot Get information about an instance
  x-api-slug: browshot
  description: Get information about an instance.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/717-browshot-com.jpg
  humanURL: http://browshot.com
  baseURL: https://api.browshot.com//api/v1//instance/info
  tags: Instance,Info
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/instanceinfo-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/instanceinfo-get-openapi.md
- name: Browshot Get all instances
  x-api-slug: browshot
  description: Get all instances.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/717-browshot-com.jpg
  humanURL: http://browshot.com
  baseURL: https://api.browshot.com//api/v1//instance/list
  tags: Instance,List
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/instancelist-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/instancelist-get-openapi.md
- name: Browshot Request a screenshot
  x-api-slug: browshot
  description: |-
    Screenshots requests to private and shared instances require a positive balance.

    *IMPORTANT*: Remember that you can only do 100 free screenshots per month. To used a premium instance, use instance_id=65 for example.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/717-browshot-com.jpg
  humanURL: http://browshot.com
  baseURL: https://api.browshot.com//api/v1//screenshot/create
  tags: Screenshot,Create
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/screenshotcreate-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/screenshotcreate-get-openapi.md
- name: Browshot Delete screenshot data
  x-api-slug: browshot
  description: You can delete details of your screenshots to remove any confidential
    information.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/717-browshot-com.jpg
  humanURL: http://browshot.com
  baseURL: https://api.browshot.com//api/v1//screenshot/delete
  tags: Screenshot,Delete
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/screenshotdelete-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/screenshotdelete-get-openapi.md
- name: Browshot Host thumbnails on your own S3 account or on Browshot.
  x-api-slug: browshot
  description: You can host screenshots and thumbnails on your own S3 account or on
    Browshot.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/717-browshot-com.jpg
  humanURL: http://browshot.com
  baseURL: https://api.browshot.com//api/v1//screenshot/host
  tags: Screenshot,Host
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/screenshothost-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/screenshothost-get-openapi.md
- name: Browshot Get the HTML code
  x-api-slug: browshot
  description: Retrieve the HTML code of the rendered page. This API call should be
    used when html=1 was specified in the screenshot request.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/717-browshot-com.jpg
  humanURL: http://browshot.com
  baseURL: https://api.browshot.com//api/v1//screenshot/html
  tags: Screenshot,Html
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/screenshothtml-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/screenshothtml-get-openapi.md
- name: Browshot Query screenshot status
  x-api-slug: browshot
  description: Once a screenshot has been requested, its status must be checked until
    it is either "error" or "finished".
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/717-browshot-com.jpg
  humanURL: http://browshot.com
  baseURL: https://api.browshot.com//api/v1//screenshot/info
  tags: Screenshot,Info
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/screenshotinfo-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/screenshotinfo-get-openapi.md
- name: Browshot Get information about screenshots
  x-api-slug: browshot
  description: Get information about the last 100 screenshots requested.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/717-browshot-com.jpg
  humanURL: http://browshot.com
  baseURL: https://api.browshot.com//api/v1//screenshot/list
  tags: Screenshot,List
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/screenshotlist-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/screenshotlist-get-openapi.md
- name: Browshot Request multiple screenshots
  x-api-slug: browshot
  description: |-
    Request multiple screenshots in one API call. The API call accepts all the parameters supported by screenshot/create.
    You can specify up to 10 URLs and 10 instances for a total of 100 screenshots in one API call.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/717-browshot-com.jpg
  humanURL: http://browshot.com
  baseURL: https://api.browshot.com//api/v1//screenshot/multiple
  tags: Screenshot,Multiple
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/screenshotmultiple-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/screenshotmultiple-get-openapi.md
- name: Browshot Search for screenshots
  x-api-slug: browshot
  description: Search for screenshots of a specific URL.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/717-browshot-com.jpg
  humanURL: http://browshot.com
  baseURL: https://api.browshot.com//api/v1//screenshot/search
  tags: Screenshot,Search
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/screenshotsearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/screenshotsearch-get-openapi.md
- name: Browshot Share a screenshot
  x-api-slug: browshot
  description: You can make your screenshots public, add notes, and share it with
    your friends and colleagues. Only screenshots which are successfully completed
    can be shared.n the thumbnail. You can take a 1024x768 screenshot, crop it to
    768x768, and get it scaled down to 300x300.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/717-browshot-com.jpg
  humanURL: http://browshot.com
  baseURL: https://api.browshot.com//api/v1//screenshot/share
  tags: Screenshot,Share
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/screenshotshare-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/screenshotshare-get-openapi.md
- name: Browshot Retrieve a thumbnail image
  x-api-slug: browshot
  description: |-
    Unlike the other API calls, this API sends back the thumbnail as a PNG file, not JSON. The HTTP response code indicates whether the screenshot was successful (200), or incomplete (404) or failed (404). If the screenshot failed or is not finished, a default image "Not found" is sent.

    You can crop your screenshots. The crop is done first, then the thumbnail. You can take a 1024x768 screenshot, crop it to 768x768, and get it scaled down to 300x300.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/717-browshot-com.jpg
  humanURL: http://browshot.com
  baseURL: https://api.browshot.com//api/v1//screenshot/thumbnail
  tags: Screenshot,Thumbnail
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/screenshotthumbnail-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/screenshotthumbnail-get-openapi.md
- name: Browshot
  x-api-slug: browshot
  description: 'A service to easily make screenshots of web pages in any screen size,
    as any device: iPhone, iPad, Android, Nook, PC, etc. Test your site on different
    devices in many resolutions.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/717-browshot-com.jpg
  humanURL: http://browshot.com
  baseURL: https://api.browshot.com//api/v1
  tags: Browshot.com
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/browshot-com/master/_listings/browshot-com/openapi.md
x-common:
- type: x-base
  url: https://api.browshot.com/api/
- type: x-blog
  url: http://blog.browshot.com/
- type: x-blog-rss
  url: http://blog.browshot.com/feeds/posts/default
- type: x-crunchbase
  url: http://www.crunchbase.com/company/browshot
- type: x-crunchbase
  url: https://crunchbase.com/organization/browshot
- type: x-developer
  url: http://browshot.com/api/documentation
- type: x-email
  url: feedback@browshot.com
- type: x-twitter
  url: https://twitter.com/BrowshotCom
- type: x-website
  url: http://browshot.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---