{
  "info": {
    "name": "Browshot Get the batch status",
    "_postman_id": "edc57eb6-faf8-466d-b23b-57586b8f9c69",
    "description": "Get the status of a batch requested through the API or through the dashboard.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Batch",
      "item": [
        {
          "id": "22a9db54-16a5-4676-be52-1d2d169e8515",
          "name": "CreateBatch",
          "request": {
            "url": "http://api.browshot.com/api/v1/batch/ceate?hosting=%7B%7D&hosting_bucket=%7B%7D&hosting_file=%7B%7D&hosting_headers=%7B%7D&hosting_height=%7B%7D&hosting_scale=%7B%7D&hosting_width=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "cookie",
                  "value": "{}",
                  "disabled": false,
                  "description": "set a cookie for the URL requested (see Custom POST Data, Referer and Cookie) Cookies should be separated by a ; - paid screenshots only"
                },
                {
                  "key": "delay",
                  "value": "{}",
                  "disabled": false,
                  "description": "number of seconds to wait after the page has loaded"
                },
                {
                  "key": "details",
                  "value": "{}",
                  "disabled": false,
                  "description": "level of information available with screenshot/info"
                },
                {
                  "key": "file",
                  "value": "{}",
                  "disabled": false,
                  "description": "text file to use"
                },
                {
                  "key": "flash_delay",
                  "value": "{}",
                  "disabled": false,
                  "description": "number of seconds to wait after the page has loaded if Flash elements are present"
                },
                {
                  "key": "format",
                  "value": "{}",
                  "disabled": false,
                  "description": "image as PNG or JPEG"
                },
                {
                  "key": "headers",
                  "value": "{}",
                  "disabled": false,
                  "description": "any custom HTTP headers"
                },
                {
                  "key": "height",
                  "value": "{}",
                  "disabled": false,
                  "description": "thumbnail height"
                },
                {
                  "key": "html",
                  "value": "{}",
                  "disabled": false,
                  "description": "saves the HTML of the rendered page which can be retrieved by the API call screenshot/html"
                },
                {
                  "key": "instance_id",
                  "value": "{}",
                  "disabled": false,
                  "description": "instance ID to use"
                },
                {
                  "key": "max_wait",
                  "value": "{}",
                  "disabled": false,
                  "description": "maximum number of seconds to wait before triggering the PageLoad event"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "name of the batch"
                },
                {
                  "key": "post_data",
                  "value": "{}",
                  "disabled": false,
                  "description": "send a POST requests with post_data, useful for filling out forms - paid screenshots only"
                },
                {
                  "key": "priority",
                  "value": "{}",
                  "disabled": false,
                  "description": "assign priority to the screenshot (for private instances only)"
                },
                {
                  "key": "referer",
                  "value": "{}",
                  "disabled": false,
                  "description": "use a custom referrer header - paid screenshots only"
                },
                {
                  "key": "screen_height",
                  "value": "{}",
                  "disabled": false,
                  "description": "height of the browser window"
                },
                {
                  "key": "screen_width",
                  "value": "{}",
                  "disabled": false,
                  "description": "width of the browser window"
                },
                {
                  "key": "script",
                  "value": "{}",
                  "disabled": false,
                  "description": "URL of javascript file to execute after the page load event"
                },
                {
                  "key": "size",
                  "value": "{}",
                  "disabled": false,
                  "description": "screenshots size - screen (default) or page"
                },
                {
                  "key": "width",
                  "value": "{}",
                  "disabled": false,
                  "description": "thumbnail width"
                }
              ]
            },
            "description": "Get hundreds or thousands of screenshots from a text file. You can use this API call or the dashboard. Unlike the other API calls, you must issue a POST request with the Content-Type \"multipart/form-data\" in order to upload the text file. The text file must contain the list of URLs to request, 1 URL per line. Failed screenshots will be tried up to 3 times before giving up."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f10de500-ac88-42d1-853a-1aa004cc5dda"
            }
          ]
        },
        {
          "id": "7edaba46-8c95-4d29-9e08-5ffd44c2605a",
          "name": "GetBatchInfo",
          "request": {
            "url": "http://api.browshot.com/api/v1/batch/info?id=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get the status of a batch requested through the API or through the dashboard."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b414076f-25df-41da-aaad-0ee546279121"
            }
          ]
        }
      ]
    }
  ]
}