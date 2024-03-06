# Sample code for the Web Widget that promote the Office add-in.

The webpage will show the add-in name, a short description of the add-in, a few details about the add-in functionality for highlight, a dropdown button to install and use the add-in and a video to demo the add-in. This is how the UI looks like.

<img alt="DemoUI.png" src="https://github.com/AmandaHan123/WebWidget/blob/main/DemoUI.png?raw=true">

![image](https://github.com/AmandaHan123/WebWidget/assets/97148607/191518de-c4b9-48b1-9b63-cd2504bd6c45)


## Usage

1. Download the .html file and go to <script> at line 55.

2. Config the paramenters under "Paramenters that need to config" part.<br>
	a. <strong>addinId</strong><br>
		This is the unique add-in ID. You can get the correct value by following below steps.<br>
		1) Go to https://appsource.microsoft.com/en-US/ from your browser.<br>
		2) Input your Office add-in name in the search bar on top center of AppSource homepage.<br>
		3) Click your add-in in the seach results.<br>
		4) The add-in information page will be automatically displayed in current tab.<br>
		5) The add-in ID is in the URL.<br>
   For example, if the URL is https://appsource.microsoft.com/en-US/product/office/WA104380862?tab=Overview, then "WA104380862" is the add-in ID that you should input for this parameter in sample code.
		
	b. <strong>addinName</strong><br>
		This is the add-in name. You can get the correct value by following below steps.<br>
		1) Go to the webpage in 2.a.4).<br>
		2) The add-in name is displayed as the title on right of the add-in icon.<br>
   For example, if the webpage is https://appsource.microsoft.com/en-US/product/office/WA104380862?tab=Overview, then "Script Lab, a Microsoft Garage project" is the add-in ID that you should input for this parameter in sample code.
		
	c. <strong>wordOnlineSupported, excelOnlineSupported, powerpointOnlineSupported, desktopSupported</strong><br>
		This is the Office products that this add-in supports. You can get the correct value by following below steps.<br>
		1) Go to the webpage in 2.a.4).<br>
		2) Click "details + support" tab on the webpage.<br>
		3) Scroll down to "Products supported" section.<br>
			- If "Word on the web" is in the list, then set wordOnlineSupported to true. Otherwise, set it to false.<br>
			- If "Excel on the web" is in the list, then set excelOnlineSupported to true. Otherwise, set it to false.<br>
			- If "PowerPoint on the web" is in the list, then set powerpointOnlineSupported to true. Otherwise, set it to false.<br>
			- If any item contains "Windows" or "Mac", then set desktopSupported to true. Otherwise, set it to false.<br>
			
	d. <strong>addinShortDescription</strong><br>
		This is the short description for the add-in which is displayed on the webpage. Please customize it as you need. 
		
	e. <strong>addinDetails</strong><br>
		This is for descriptions about the add-in functionalities displayed on the webpage. It is implemented as 2D Array. Each row is one piece of description. The first column is the highlighted text for summary of current description, and the second column is for more explanation for currect description. Please customize the text as you need.
		
   Note: It is free for you to add/remove the row count to display more/less descriptions. But if you prefer to not use 2D Array, please also update the for Loop in setContent() which is located at line 95 to line 103. 
		
	f. <strong>demoVideoLink</strong><br>
		This is for the demo video that display on the webpage. Please customize it as you need.
		
4. Save the html file and open by browser. Verify the UI and dropdown links works for your scenario.

5. Make any additional changes to the sample code as you need, and integrete it into your website.

## Special Notice

The project is currently for experiment and test only. 

The deeplink for the dropdown button is possible to change in the future when needed. In the case it changes, any user of this sample code may need to update your code.

The deeplink can successfully open an Office document with your add-in and the end users can use your add-in for below scenarios only.

1. The add-in is public published, so that it can be found from Office AppSource https://appsource.microsoft.com/.

2. The Office store is enabled for the end user.


