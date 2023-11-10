# flask_5_tailwind
HHA 504 Assignment 5

# CDN Setup

For Azure I went to the Storage Account section to create a new one that I called "johnahicdn". Once it was created I then went to the section called Containers under Data Storage and created  created a new container called "test-ahi-cdn". To allow me to create the continer I did have to change some secureity settings. In the storage account I went into security and made sure to enable "Allow Blob anonymous access". This would then allow me to create a container. 

I then went into the container to upload a stock video of someone working on the computer to test out how it would upload. I didn't run into any issues with this. 

After that I went into the Security + networking section of the storage account and clicked on "Front Door and CDN" service. To create a new end point I picked the Azure CDN as a service type and called it 'flask-john-cdn-test'. I used the Standard Microsoft pricing tier to keep expenses low. The hostname created was 'john-cdn.azureedge.net'. 

# Flask Setup

I then used the video tag in the 'index_tailwind.html' file to allow it to show the video properly and used the url I got from my cdn that was connected to my storage container 'https://john-cdn.azureedge.net/test-ahi-cdn/office_-_6395%20(540p).mp4'. 

![Video Tag in HTML Screenshot](Screenshots/Video%20Tag%20in%20html.png)

Once it was all up and running I was able to see in the Inspect view of the browser that the picture was indeed getting pulled from the CDN and how fast it took to load in milliseconds. 

Here I added a screenshot of it. 
As a side not I figured out how to embed pictures into the readme file for easier viewing of the screenshots.
![Network Speed (Inspect View) Screenshot](Screenshots/Network%20Speed%20(Inspect%20View).png)
