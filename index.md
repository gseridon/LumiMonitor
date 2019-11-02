<b>Entry06: 11/01/2019</b>

I'm having a lot of problems with the Raspberry Pi at the moment, and it is severely delaying my progress with the course.
I have set up an OS for the pi during the break, but the pi heats up extremely quickly within the first few minutes of being powered up. The microSD card that I was using for the pi burned out a few days ago as well. This pressured me to purchase another SD card last minute, which did not arrive until Wednesday of this week. This new SD card was also uploaded with the operating system, which the balenaEtcher is verifying to be acceptable to use. However, when I try to install the operating system now, the raspberry pi would still heat up very quickly, and it would show an error on the screen. I have tried several times to reupload the operating system into the SD card, each time the disk imager would verify that the loading was successful (I even used a different SD card from a friend on different attempts). But the same thing occurs, the raspberry pi would continuously show an error and stopping me from installing the operating system, thus halting my progress on the assignment.

I'm considering on just purchasing the new Raspberry Pi 4, as I suspect that the Raspberry Pi 3 that I have purchase is faulty and corrupting the SD cards that I use for it. I will be purchasing the Raspberry Pi 4 this weekend and hope that it will arrive quickly, so that I can set up operating system once more and run the code for the si7021 temperature/humidity sensor.

Financial wise, things have taken a turn for the worse. While I will be attempting to refund the Raspberry Pi 3, I have purchased a micro SD card in the process of troubleshooting my problems with the Pi. I will also be looking to purchase the complete set of the Raspberry Pi 4 for this weekend in hopes that I will be able to catch up with my schedule.

This week's purchases:
- MicroSD card: $11.97 CAD + $1.56, free shipping
- Raspberry Pi 4: $134.99 CAD + $17.55 tax, free shipping

Schedule-wise, I am a behind on loading the operating system and the breadboard milestone, as I have not been able to get the RP3 to work properly. This puts me approximately two weeks behind schedule. However, if I should get the new RP4 by this weekend, I will be attempting to catch up on installing the OS and connecting the sensor to the breadboard by next week. If all goes well, I will be able to get back on schedule.

I have found the code for the si7021 temperature/humidity sensor as well, and will be attempting to use this code to test the sensor when the RP4 has arrived and set up properly.
It is uploaded <a href="https://github.com/gseridon/LumiMonitor/blob/master/Software/si7021_test_code.py">here</a>.


<b>Entry06: 10/15/2019</b>

  The schematic of the sensor and raspberry pi:
  <img src="https://raw.githubusercontent.com/gseridon/LumiMonitor/master/Images/SchematicV1.png">
  
  The breadboard connection: 
  <img src="https://raw.githubusercontent.com/gseridon/LumiMonitor/master/Images/BreadboardV1.png">
  
  The PCB design:
  
  <img src="https://raw.githubusercontent.com/gseridon/LumiMonitor/master/Images/PCBV1.png">

The design of the board was fairly simple. Vin is the power pin, and it is connected to the 3 VDC pin on the raspberry pi.  The sensor's 3v3 pin is not used. The GND pin is the common ground for the power and logic.  The SCL pin is the I2C clock pin, which is connected to the raspberry pi's I2C clock line. The SDA pin is the I2C data pin, which is connected to the raspberry pi's I2C data line. These pins are represented by headers instead of the actual sensor/raspberry pi; the 5 pin header is for the temperature/humidity sensor, while the 6 pin header is for the raspberry pi.

As of today, I am right on time according to my schedule. I have the breadboard, schematic, and PCB designed, and it is ready to be printed. I will be sending the gerber files to the prototype lab to have my PCB created.  I had a few problems with my initial design of the PCB, but after attending the class session and getting some feedback from Professor Medri, I was able to correctly redesign my PCB.
 
Over this past weekend, I had to re-order my Raspberry Pi as the parcel has been lost in the mail and could not be retrieved. Amazon was able to resend my purchase, and I have acquired the Raspberry Pi and the sensor by Sunday, October 13. There were no additional charges to this transaction, so I am on track with my financial status.  All the images (schematic, PCB, breadboard) and files (FZZ file using the pi and without it) regarding the hardware of the project has been uploaded into my repository, with the appropriate links in the blog post:
  
  <a href="https://github.com/gseridon/LumiMonitor/blob/master/Images/SchematicV1.png">Schematic</a>, 
  <a href="https://github.com/gseridon/LumiMonitor/blob/master/Images/BreadboardV1.png">Breadboard</a>,
  <a href="https://github.com/gseridon/LumiMonitor/blob/master/Images/PCBV1.png">PCB</a>
  
  
  The two fritzing files; one with the raspberry pi, and one without it (just for the PCB design):
  <a href="https://github.com/gseridon/LumiMonitor/blob/master/Electronics/GinoSeridon_TemperatureHumiditySensorV1.fzz">With Pi</a>,
  <a href="https://github.com/gseridon/LumiMonitor/blob/master/Electronics/GinoSeridon_TemperatureHumiditySensorWithoutPiV1.fzz">Without Pi</a>
  

<b>Entry05: 09/29/2019</b>

  I have placed my order for the Raspberry Pi, the webcam, and the temperature sensor. I have also updated the project budget to include the additional purchase of the Raspberry Pi.

Proof of Purchase: <a href="https://github.com/gseridon/LumiMonitor/blob/master/Images/AmazonOrder.png">Amazon</a>, 
<a href="https://github.com/gseridon/LumiMonitor/blob/master/Images/DigikeyOrder.png">Digikey</a>

<b>Entry04: 09/24/2019</b>

  Today my group members and I had our meeting with our collaborator, running our ideas through him and getting some feedback from him. He was very enthusiastic towards our ideas and offers his full support to the direction of our project.
  
  I have uploaded the project budget for the LumiMonitor's temperature sensor, with the webcam price included.
  
  Link: <a href="https://github.com/gseridon/LumiMonitor/blob/master/Documentation/Project%20Budget.pdf">Project Budget PFD</a>

<b>Entry03: 09/10/2019</b>

  Submission of the hard copy printout of the project proposal. I have completed a project schedule in the form of a gantt chart and have converted it into a PDF. This version of the schedule is uploaded into the repository and can be found <a href="https://github.com/gseridon/LumiMonitor/blob/master/Documentation/LumiMonitorScheduleGanttChart.pdf">here.</a> 
  
  This schedule is based off the due dates outlined in the <a href="https://six0four.github.io/ceng317/">CENG317 Course Repository.</a>

<b>Entry02: 09/09/2019</b>

  Completed the proposal content and the project proposal, and converted them into a PDF file. These files, along with the Excel  proposal sheet, are uploaded to my online repository, in the "Documentation" folder. I have also completed creating all the different folders needed in the repository today, leaving a note in each folder to dictate the folder's future content.
  
  The links for the uploaded documents are as follows:
  - <a href="https://github.com/gseridon/LumiMonitor/blob/master/Documentation/ProjectProposalGinoSeridonLumi.pdf">Project Proposal (PDF)</a>
  - <a href="https://github.com/gseridon/LumiMonitor/blob/master/Documentation/ProposalContentGinoSeridonLumi.pdf">Proposal Content (PDF)</a>

  Lastly, I have activated the github master branch for the repository, enabling me to publish the repository website.
  
  Link: <a href="https://gseridon.github.io/LumiMonitor">https://gseridon.github.io/LumiMonitor</a>

<b>Entry01: 09/05/2019</b>

  First day working on the Lumi Monitor project. I did a bit of research for the project to try and brainstorm some ideas for it. I have created a repository today, as well as having completed my registration along with my group members on Riipen. I'm filling out the proposal with content pretaining to the Lumi monitor and will be uploading the finished documents on github.
