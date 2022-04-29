# Media Content Engagement Predictor

The business challenges which this tool address is as mentioned below:

a. Email Brand Reputation: Organization sends lot of emails to the target audiences with an objective to engage them with their marketing content to increase revenue for their organization. The size of this target audience varies from few hundreds to millions. The organization uses their domain while sending an email example contactus@organizationname.com so that receiver (audience) knows the brand who is sending them an email. When these email land in the email box of the gmail, Microsoft or other email server providers of the target audience, the receiver domain get to know that a bulk email is being sent to their domain (like gmail, Microsoft). Now, if the response in terms of open and click (engagement) of the email (marketing email) is not good these receiver domain start decreasing the reputation of the sender domain. If this continues based on low rate of the engagement the receiver domain will start sending these emails to spam folder in place of the inbox. This result is reputation loss for the sender brand. Thus, organization wants to send email to only those people that have good likelihood to engage with the email.

b. Optimized Marketing Spend: The add are served by organizations on the add platforms like social media and programmatic platform with the objective that target audience click on the add. On click, the target audience are diverted to the organization website for up sale and cross sale of their product or services. For each of these add to render on the add platform a huge $ amount is spent by the organizations. Organizations wants to save on this spend by serving add only to the people that have good likelihood to click.

c. Choice of the Media Channel: Target audience always have personal liking about the channel they engage with more. Some engage more with email while others engage more with social websites or domain websites. Finding the likelihood on the preferred media channel for engagement is always critical.

# How to Install:

The code is the "Social Media Python CODE.txt" file needs to be converted into the right python extension which can be utilized by complier. Anaconda is a good platform to run this code. The steps to run the code in the Anaconda Python platform is as mentioned below:

Step 1: Download Anaconda

Go to Anaconda.com

Step 2: Select Windows

Make sure that the anaconda distribution is for windows by clicking on the Windows icon since we are downloading it for windows 10.

Step 3: Check the System Type

We need to know the system type so as to select the appropriate .exe installer for the system. If you already know your system type, you can go to step 4. Else follow the steps below:

a. Right Click on My Computer

b. Go to Properties

c. In the System Section, Check the System type. For me, it is an x64 based processor.

Step 4: Download the .exe Installer.

Download the most recent release of python. At the time of writing this post, it is python 3.7. The download file is around 462 MB, so it may take some time for Anaconda to download. If your system type is x64, directly click the download button; else, click on 32-bit Graphic Installer.

Step 5: Run the Downloaded .exe File

a. After the file is downloaded, open and run the .exe installer, you will get a Welcome window.

b. Click on Next. You will get a window showing the License Agreement.

c. Click on I Agree.

d. All Users is not recommended as most of the time; people don’t have the admin rights, so Select “Just Me” and Click Next.

e. Select the Destination Folder in which you want to install Anaconda distribution and Click Next.

Do not select “Add Anaconda to my PATH environment variable ” as most of the user does not have administration rights. Select the checkbox “Register Anaconda as my default Python 3.7”. Click Install. This will install Anaconda in your system.

Step 6: Open Anaconda Prompt

a. Once the installation of the anaconda is completed. Go to windows start and select the anaconda prompt.

b. This will start the anaconda prompt window, which looks like a black window, as shown in the snapshot below.

Note that you will see Anaconda and Anaconda Prompt. It’s important to know that Anaconda Prompt is a command-line shell while Anaconda is a python distribution GUI.

Step 7: Run the Python Interpreter

Type the python command in the anaconda prompt window and hit enter:

a. Note the python version. For me, it is showing “Python 3.7.4”. The greater than symbols >>> indicates that the python interpreter is running.

b. That’s it. Now you can run the python commands. Try to import “this” by typing. Import this on python interpreter. You should see the Zen of Python by Tim Peters.

c. You can close the python interpreter by typing “exit()” and press enter.

d. To Close the Anaconda Prompt, you can either close it using the command exit or use the mouse to close.

To Restart the Anaconda Prompt and use python, you can start selecting Anaconda Prompt and type the “python” command to start the python interpreter. If you have reached this step, then you have Installed Anaconda Python Successfully on your system.

If you want to have another version of python, say pytho2.7, in your project, then you can create a separate environment with python2.7. To do so, use the following command : conda_create name_env_name_python

Running this will create a new env in anaconda named as “env_name” to start the environment type.

This will start the environment, which will have python 2.7. Since the conda environment is independent of each other, you create any number of the environment with different versions of python or any other packages.


# How to use:


a. Inputs

Campaign Data
The campaign file will have the attributes related to the campaign like campaign name, subject line, content, campaign date, sender domain , content classification into tone and topic etc

Media Transaction
Media data set will have the information about the media metadata like recipient that receive campaign and his behavior towards that campaign in terms of open and click.

The above two input file will bring all the required data set needed to train the ML model.

b. Algorithm

Ensemble model of XG and LightXB boot are used and Algorithm will have following steps:

Import Python Libraries & Setting Environment Parameters

Loading Training & Test Data Set

Similarity Algorithm

Covert Sent Date to Hash Key

Extracting Sent Date Features

Deriving features based on the open and click events

Merging Test and Train Data Set

Filling Na for Open and Click

Merging Campaign Master and Email Data Set

Sort by Recipient id and sent date. This is needed to correctly count user_date_diff and user_camp_diff

Subject Line and Pre header Text encoding

Date and NLP Functions

Features on Campaign dates

Converting it to one click per email

Derived features

Applying functions

Using dummies to create the Subject Line and Pre header Text encoding encoding

Feature Engineering on HCP Profile Attributes

Tactic Code Encodings

Removing Unwanted Fields 1

Business Unit and Media Channel Features

Tone and Topic Features

Removing Unwanted Fields 2

Removing Unwanted Fields 3

Removing Unwanted Fields - Click Features

Campaign ID encoding

Sent Date Features (For time bin)

Remove Camp IDs field

Building Brand Encodings

c. Output

The out of the algorithm will be in the form of the receipient id and percentage of likehood for the receipient to engage with marketing content.


# Next steps for this asset:

Currently this tool is doing the prediction based on the inputs of the recipient and it's behavior by media transaction records. This tool will be further extended to do the following.

a. Improve User Interface 

b. Scalable to other media tactic like banner, programmatic add and enewletter


