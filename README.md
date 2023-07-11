[https://apify.com/epctex/instagram-video-downloader](https://apify.com/epctex/instagram-video-downloader?fpr=yhdrb)

# Actor - Instagram Video Downloader

## Instagram Video Downloader

Since Instagram doesn't provide a good and free API, this actor should help you to download videos from Instagram.com

The Instagram Video Downloader supports the following features:

-   Download Video - If you want to get videos on a certain URL, just type the URL.

## Bugs, fixes, updates, and changelog

This scraper is under active development. If you have any feature requests you can create an issue from [here](https://github.com/epctex/instagram-video-downloader/issues).


## Input Parameters

The input of this scraper should be JSON containing the list of pages on Instagram.com that should be visited. Required fields are:

- `startUrls`: (Optional) (Array) List of Instagram URLs. You should only provide post URLs.

- `proxy`: (Required) (Proxy Object) Proxy configuration.

- `extendOutputFunction`: (Optional) (String) Function that takes a JQuery handle ($) as an argument and returns an object with data.

- `customMapFunction`: (Optional) (String) Function that takes each object's handle as an argument and returns the object with executing the function.

This solution requires the use of **Proxy servers**, either your own proxy servers or you can use [Apify Proxy](https://www.apify.com/docs/proxy).

### Tip

When you want to scrape over a specific list URL, just copy and paste the link as one of the **startUrl**.

### Compute Unit Consumption

The actor is optimized to run blazing fast and scrape as many items as possible. Therefore, it forefronts all the detailed requests. If the actor doesn't block very often it'll scrape 1 video under 45 seconds with ~0.01-0.02 compute units.

### Instagram Video Downloader Input example

```json
{
    "startUrls": [
        "https://www.instagram.com/p/CuKHeY_PLbZ/"
    ],
    "proxy": {
        "useApifyProxy": true
    }
}
```

## During the Run

During the run, the actor will output messages letting you know what is going on. Each message always contains a short label specifying which page from the provided list is currently specified.
When items are loaded from the page, you should see a message about this event with a loaded item count and total item count for each page.

If you provide incorrect input to the actor, it will immediately stop with a failure state and output an explanation of what is wrong.

## Instagram Video Downloader Export

During the run, the actor stores results into a dataset. Each item is a separate item in the dataset.

You can manage the results in any language (Python, PHP, Node JS/NPM). See the FAQ or <a href="https://www.apify.com/docs/api" target="blank">our API reference</a> to learn more about getting results from Instagram Video Downloader.

The structure of each item in Instagram looks like this:

### Item Detail

```json
{
	"sourceUrl": "https://www.instagram.com/p/CuKHeY_PLbZ/",
	"downloadUrl": "https://api.apify.com/v2/key-value-stores/fb731f08-ed1b-4b59-8774-4ef2ab7dd261/records/c5cb8c4312b750252ac72f9e3cacdd30"
}
```

## Contact 
Please visit us through [epctex.com](https://epctex.com) to see all the products that are available for you. If you are looking for any custom integration or so, please reach out to us through the chat box in [epctex.com](https://epctex.com). In need of support? [devops@epctex.com](mailto:devops@epctex.com) is at your service.
