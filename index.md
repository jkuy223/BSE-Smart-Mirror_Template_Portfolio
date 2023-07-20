# Gerardo's Project
My project was a smart mirror. I had to connect a display to a raspberry pi which was my first time using one. I used it to run the base code for my smart mirror then made a case to hold the display. I mainly stuggled with coding and inputing commands. I didn't understand much of the steps I would see online so asking for help from instructors was key. I completed my project up to the case which holds my lcd display and I like how my smart mirror templates looks.

You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions:
```HTML 
<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->
```

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Gerardo G | John H. Francis Polytechnic | Areospace Engineering | Incoming Senior

**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

![Headstone Image](logo.svg)
  
# Final Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your final milestone, explain the outcome of your project. Key details to include are:
- For my my final milestone I have added my case for my display which makes adding other things much easier so while I don't have the mirror my final template for the display is good
- Getting to this step was really acomplishing as I struggled with the code a lot and would constalty mess up my whole template for the mirror but anyway I added and fixed modules or existing modules and have everything I want in my code for the mirror
- this program has let me learn the issues you can face in this field and where my strengths are and what i need to work on more. This project specifcally taught me that coding and knowing more about the coding vocabulary and overall terms and knowledge is very important for engineers



# Second Milestone

**
*

<iframe width="560" height="315" src="https://www.youtube.com/embed/y3VAmNlER5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your second milestone, explain what you've worked on since your previous milestone. You can highlight:
- For my second milestone I have added more modules that do actions like connect people to my wifi or ask trivia questions. 
I also setup the correct time and weather from the base template.
-The third party module integration was diffucult as I had trouble with the code and certain modules. I got through this by refering to the base code at all times to make sure I wasn't messing up the main code.
- The third party modules got easier to integrate the more I added as the process is usally the same. 
-I now have to just add on the actual mirror on the display and make sure the smart part of the mirror is visable through the mirror.

# First Milestone

**For my first milestone I set up my magic mirror software and the display with the raspberry pi. Initially I was confused with where to start but once I figured that out everything went pretty smooth. I set up the code for the magic mirror following the guide on Magic Mirror builders for raspberry pie and connected my display to my raspberry pi so I could actually see the magic mirror base template. After this 
I still have to add more modules and actually set up the pyschical mirror on the display.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/CaCazFBhYKs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your first milestone, describe what your project is and how you plan to build it. You can include:
- For my first milestone I set up my magic mirror software and the display with the raspberry pi
- Initially I was confused with where to start but once I figured that out everything went pretty smooth
- I set up the code for the magic mirror following the guide on Magic Mirror builders for raspberry pie and connected my display to my raspberry pi so I could actually see the magic mirror base template
- After this I still have to add more modules and actually set up the pyschical mirror on the display.

# Schematics 
Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser. 

# Code
Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. 

```c++
void setup() {
  // put your setup code here, to run once:
{
			module: "alert",
		},
		{
			module: "updatenotification",
			position: "top_bar"
		},
		{
			module: "clock",
			position: "top_left"
		},
		{
			module: "calendar",
			header: "US Holidays",
			position: "top_left",
			config: {
calendars: [
					{
						fetchInterval: 7 * 24 * 60 * 60 * 1000,
						symbol: "calendar-check",
						url: "https://ics.calendarlabs.com/76/mm3137/US_Holidays.ics"
					}
				]
			}
		},
		{
			module: "compliments",
			position: "lower_third"
		},
		{
			module: "weather",
			position: "top_right",
			config: {
				weatherProvider: "openweathermap",
				type: "current",
				location: "New York",
				locationID: "5128581", //ID from http://bulk.openweathermap.org/sample/city.list.json.gz; unzip the gz file and find your city
				apiKey: "98e6e54a5c8e2b3dce3259409a6a7e4f"
			}
		},
		{
			module: "weather",
			position: "top_right",
			header: "Weather Forecast",
			config: {
				weatherProvider: "openweathermap",
				type: "forecast",
				location: "New York",
				locationID: "5128581", //ID from http://bulk.openweathermap.org/sample/city.list.json.gz; unzip the gz file and find your city
				apiKey: "98e6e54a5c8e2b3dce3259409a6a7e4f"
			}
},
		{
			module: "newsfeed",
			position: "bottom_bar",
			config: {
				feeds: [
					{
						title: "New York Times",
						url: "https://rss.nytimes.com/services/xml/rss/nyt/HomePage.xml"
					}
				],
				showSourceTitle: true,
				showPublishDate: true,
				broadcastNewsFeeds: true,
				broadcastNewsUpdates: true
			}
		},
		{
			module: "MMM-GoogleDriveSlideShow",
			position: "bottom_bar",
			config: {
				rootFolderId: null,
				maxFolders: 10, 
				maxResults: 100,
				playMode: "AUTO",
				nextOnNotification: null,
				stopOnNotification: null,
				startOnNotification: null,
				refreshDriveDelayInSeconds: 24 * 3600, 
				refreshSlideShowIntervalInSeconds: 10,
				maxWidth: "800",
				maxHeight: "600",
				theme: "whiteFrame",
				opacity: 1,
				debug: false
			    }
			},
		    {
    module: 'MMM-WiFiPassword',
    position: "top_left",
 config: {
        //See 'Configuration options' for more information.
        network: "Oscuro_is_the_best_period", 
        password: "Kirby_cutie@xxx",
         }
      },
	]
};

  Serial.begin(9600);
  Serial.println("Hello World!");
}

void loop() {
  // put your main code here, to run repeatedly:

}
```

# Bill of Materials
Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. 

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Lcd Display | This is where the smart mirror code is displayed onto the mirror | $49 | <a href="https://www.walmart.com/ip/Dioche-LCD-Touch-Screen-Capacitive-Touch-Screen-7-Inch-1024x600-LCD-Touch-Screen-Display-With-Acrylic-Shell-For-4B-3B-3B/199167286?wmlspartner=wlpa&selectedSellerId=101093676&&adid=22222222227199167286_101093676_157071512768_18742549668&wl0=&wl1=g&wl2=c&wl3=666037187212&wl4=pla-2162313096121&wl5=9031202&wl6=&wl7=&wl8=&wl9=pla&wl10=468006167&wl11=online&wl12=199167286_101093676&veh=sem&gclid=Cj0KCQjwk96lBhDHARIsAEKO4xYuTQBuy95KODaSyeM-1rDp51xMU9huGjWYHMmyIwW1BbBtJ8ympJ0aAgz0EALw_wcB&gclsrc=aw.ds"> Link </a> |
| 7 inch case | Frame for the Lcd Display | $12 | <a href="https://www.amazon.com/Longruner-Raspberry-Various-Systems-LSC7B-1/dp/B07KRX3QCQ/ref=pd_bxgy_vft_none_sccl_1/142-0985611-7894557?pd_rd_w=iX9Wr&content-id=amzn1.sym.26a5c67f-1a30-486b-bb90-b523ad38d5a0&pf_rd_p=26a5c67f-1a30-486b-bb90-b523ad38d5a0&pf_rd_r=M5D9MWHEWDJDJ7RF6NEH&pd_rd_wg=4ZJB4&pd_rd_r=d39acf82-1e09-4218-b1d1-e74f0d003902&pd_rd_i=B07KRX3QCQ&psc=1"> Link </a> |
| Raspberry Pi 4 Starter Kid | The Raspberry Pi is the computer for the mirror | $119 | <a href="https://www.canakit.com/raspberry-pi-4-starter-kit.html"> Link </a> |

# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.
