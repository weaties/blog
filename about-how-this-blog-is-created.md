---
share: true
---



**Starting My Own Blog: A Practical Approach to Personal Content**

I'm launching this blog for a simple purpose: to share letters and photos with family and friends and document my upcoming trips.

**A Practical Solution for a Communication Problem**

I faced challenges when including photos in emails that I would create in the application “drafts” on my Mac or iPhone. It was a tedious process. Writing the content in Obsidian and then trying to add images wasn't any better.

I documented my [2021 road trip](weaties2021roadtrip.com) on WordPress. It worked well enough, but I couldn't control or back up my content. WordPress owned it. I wanted to find an alternative where I had full control.  Not to mention that I needed to be online in order to write the posts, and that was sometimes just not available to me.

**Discovering New Tools: Obsidian, GitHub, and Jekyll**

I’ve been a heavy user of [obsidian](https://obsidian.md) for a couple of years.  It has become the app I use for taking meeting notes, my daily journal, planning, etc.  and it has really infiltrated my life as the place that I keep my stuff.

It was a game-changer when I found the [GitHub Publisher for Obsidian](https://github.com/ObsidianPublisher/obsidian-github-publisher), which eased the process of including images. GitHub Publisher combined with GitHub Pages allowed me to host my content online while keeping full control.   This same setup works from my Mac as well as from my iPhone and iPad.

Jekyll templates provide flexible options for website design. They're easy to use and make content presentation a breeze.

If you wanted to host a blog on GitHub, you could skip the whole obsidian and GitHub publisher step, and just maintain all of you writings as files in GitHub, and all of the workflows that you might use for that would work.   So adoption of Obsidian is not _required_ by any stretch of the imagination, to have a blog on hosted on GitHub.

In conclusion, this blog gives me the control to personalize my content and the convenience to manage it efficiently. Here's to more streamlined communication and documentation!

### Using templates 
I am using the [templater obsidian plugin](https://github.com/SilentVoid13/Templater) and the [quickadd obsidian plugin](https://quickadd.obsidian.guide/docs/) to help with the creation of the blog entries.  

I have created a quick add action 

![CleanShot 2024-02-03 at 16.26.34@2x](./attachments/CleanShot%202024-02-03%20at%2016.26.34@2x.png)

that uses a template to create a new file, in the correct directory, with the front matter that I need.

Because the github.io blog has troubles linking to files that have spaces in the name (and I am not exactly why).  I am using a bit of templater trickery to rename the file, and convert the spaces in the file name, to dash's

![CleanShot 2024-02-03 at 16.25.08@2x 1](./attachments/CleanShot%202024-02-03%20at%2016.25.08@2x%201.png)
With this trick, the title maintains the spaces, but the name of the file has them swapped.

### Creating the index page.

In order to create an index page that has a list of all of the letters that I have publihsed. I am using the [dataview obsidian plugin](https://blacksmithgu.github.io/obsidian-dataview/) to list the files.

![CleanShot 2024-02-03 at 16.30.23@2x 1](./attachments/CleanShot%202024-02-03%20at%2016.30.23@2x%201.png)

and then to make things work correctly I told the github publisher to convert the dataview results to markdown when it publishes it. ![CleanShot 2024-02-03 at 16.33.48@2x](./attachments/CleanShot%202024-02-03%20at%2016.33.48@2x.png)

## Location Management
As a part of this, i would also like to be able to use the [obsidian mapview plugin](https://github.com/esm7/obsidian-map-view) to be able to show where all of these notes were created, and to be able to see them on the map.   To do that I add the `location:` property to the [obsidian front matter](https://www.wundertech.net/yaml-front-matter-in-obsidian/)  and I use [Map View GeoHelper](https://esm7.github.io/obsidian-geo-helper) in order to get my current location, and insert it into that front matter.

## Sharing the tracks of our travels
we use [giagps](https://www.gaiagps.com/) to keep track of our travels.  This is an awesome piece of software that runs as an app on our iphone, it's a website, the whole nine yards.  There are a couple of cool things that it does for us.

1. It can add all of the photos you take during your trip to the track of the trip.
2. You can share your tracks from the website, with all of the details.
3. you can embed a map, using iframes, of your track into a markdown file, and have that published.


<iframe src="https://www.gaiagps.com/public/h0uSbhAYJn9hJ5tS3krCuthd/?embed=True" style="border:none; overflow-y: hidden; background-color:white; min-width: 320px; max-width:840px; width:100%; height: 420px;" seamless />

> this is an example of one of the trips Catherine and I took in the summer of 2023. 

so there are a couple of problems here.

1. nothing is showing up on the published blog _after_ the iframe.   that's gotta get solved
2. the iframe is not included when I mail the contents of the page


[todolist](./todolist.md)