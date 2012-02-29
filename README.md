## Soundcloud CLI tool
### Authors: brentc4m, ngokevin, uberj, thedjpetersen (no order)

edit: Soundcloud has been integrated into youtube-dl

A little command line tool for working with Soundcloud.

You can either pass in a direct URL to a Soundcloud song or you can pass in any
link that may possibly contain Soundcloud URLs and the script will scrape for 
the links and download them all at once. If you pass in both options, a page
and a URL, it would download the URL and any URLs found within the page.

USAGE: soundcloud-dl -u [URL] -p [PAGE_WITH_URLs]

### Download a user's favorites

Pass a public username to the -f option to download that user's favorites. The
username should be the last part of their profile link. For example,

`python soundcloud-dl -f brentc4m`

### Keep track of downloaded files

Pass a file name to the -t option to record which Soundcloud URLs have been
downloaded and skip any URLs found in the file already. This works well with
downloading favorites. For example,

`python soundcloud-dl -f brentc4m -t finished_urls`
