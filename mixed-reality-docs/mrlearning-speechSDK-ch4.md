## Exploring the Speech Services Intent feature

In this lesson, we'll explore the Speech Services Intent feature. We'll set up our Azure LUIS Portal, setup our Intent/Entities/Utterances, publish our Intent Resource, connect our Unity app to our intent resource, and make our first Intent API call.

1. Allow your machine to enable dictation. To do this, go to Windows Settings, select Privacy. Then select Speech, and Inking & Typing. Turn on speech services and typing suggestions.

![Module4Chapter4step1aim](images/module4chapter4step1aim.PNG)

![Module4Chapter4step1bim](images/module4chapter4step1bim.PNG)

![Module4Chapter4step1cim](images/module4chapter4step1cim.PNG)

> Note: For information on how to do this on a Mac/Macbook, click [here](linkgoeshere).

2. Log into the [Azure Portal](https://portal.azure.com/). Once you are logged in, click on Create a resource, and search for Language Understanding, and click Enter.

![Module4Chapter4step2im](images/module4chapter4step2im.PNG)

3. Click the Create button to create an instance of this service. Name your project Speech_SDK_Learning_Module, and select Pay As You Go.

![Module4Chapter4step3aim](images/module4chapter4step3aim.png)

![Module4Chapter4step3bim](images/module4chapter4step3bim.PNG)

4. Select yourrRegion. For the purpose of this tutorial, select (US) West US. Then choose F0 for the pricing tier. Now click Create (located in the bottom left corner) to create the resource.

   >  Note: Once you have clicked Create, you'll have to wait for the service to be created, which might take a minute.

5. A notification appears in the portal once the resource is created. Click on this notification, and select Go to Resource.

6. From the Quick Start page in your LUIS API service, navigate to the first step, grab your keys, and click keys (you can also achieve this by clicking the blue hyperlink keys shown in the image below). This reveals your service, Keys. Save a copy of one of the keys so you can use it later in the application.

![Module4Chapter4step6im](images/module4chapter4step6im.PNG)

7. G back to the Quick Start page under Section 2b, click on Language Understanding Portal (shown in the image above to be redirected to the webpagesd, which you used to create your new service within the LUIS application.

> ote: Upon reaching the Language Understanding Portal, you might need to login. If you are not, with the same credentials as your Azure portal. If this is your first time using LUIS, you will need to scroll down to the bottom of the welcome page, to find and click on the Create LUIS application button.
                                                                                                                                                                 
8. Once logged in, click My Apps (if you are not in that section currently). You can then click on Create new app. Name the new app Speech SDK Learning Module. Add Speech SDK Learning Module to the description field, as well. Then click done.

![Module4Chapter4step8aim](images/module4chapter4step8aim.PNG)

![Module4Chapter4step8bim](images/module4chapter4step8bim.PNG)

> Note: If your application is supposed to understand a language different from English, you should change the Culture to the appropriate language.

9. Click Build located in the top right.

10. Under App Assets on the left, select Intents. Then click Create New Intent, and name it PressButton. 

![Module4Chapter4step10im](images/module4chapter4step10im.PNG)

> Note: it is important to use the names of Intents and Entities used in this tutorial because the Lunarcom application refences  them by name.  For other projects, naming conventions can be whatever you choose. 
>
> Note: you should now have two intents: PressButton and None.
11. Under App Assets on the left, select Entities, and click Create New Entity, and name it Action. Keep the Entity Type as Simple.

![Module4Chapter4step11im](images/module4chapter4step11im.PNG)

12. Click “Create New Entity” again and name it “Target” and keep the Entity Type as “Simple” as well.

![Module4Chapter4step12im](images/module4chapter4step12im.PNG)

13. Under App Assets on the left, select "Intents" then click on your "PressButton" Intent that you created in step 10.

![Module4Chapter4step13im](images/module4chapter4step13im.PNG)

14. Click on the View options drop-down on the right, and select Show Entity Values.

    ![Module4Chapter4step14aim](images/module4chapter4step14aim.PNG)Click on the Enter an example… textbox. Then, enter the following utterances: 

![Module4Chapter4step14bim](images/module4chapter4step14bim.PNG)

15. Click on the View options drop-down on the right, and select Show entity names.

![Module4Chapter4step15im](images/module4chapter4step15im.PNG)

16. Ensure that each of the ten utterances have the following entity labels in the following places by 1) clicking on words that are mislabeled and, in the pop-up, selecting remove label, and 2) clicking on words that should be labeled and, in the pop-up, selecting the appropriate label.

![Module4Chapter4step16im](images/module4chapter4step16im.PNG)

17. Now, to publish the model, click Train in the top right. Then, once it has finished processing, click Test in the top right.

![Module4Chapter4step17im](images/module4chapter4step17im.PNG)

18. Enter in Select the launch button in the textbox.

> Note: We did not add Select as an action in any of our utterances. But if you click on Inspect, the model recognized Select as an action entity.
>
> ![Module4Chapter4noteim](images/module4chapter4noteim.PNG)

19. Now, click publish in the top right. Ensure the drop-down says Production, and click Publish from the pop-up as well. 

![Module4Chapter4step19im](images/module4chapter4step19im.PNG)

20. Once published, a green bar will appear at the top of the page. Click on the green bar to be taken to the Manage page. 

![Module4Chapter4step20im](images/module4chapter4step20im.PNG)

21. Click Keys and Endpoints under Application Settings to the left. Then, set the drop-down to Publish To as Production. Set the time-zone to match yours, and check the box to include all predicted intent scores. Lastly, Click on Assign resource.

![Module4Chapter4step21im](images/module4chapter4step21im.PNG)

22. Select tenant from the first dropdown, and select Pay-as-you-go in the Subscription Name drop-down. Under LUIS resource name, choose the resource that we created above in steps 1-5. Then, click on "Assign resource." 

![Module4Chapter4step22im](images/module4chapter4step22im.PNG)

> Eote: ensure to copy and save the Endpoint URL associated with the resource we just assigned so that it is easily accessible for the next section.
>
> Note: for the tenant name, put your corporation or profile that you created for this application.

23. Now, open the new app in Unity, and select the Lunarcom_Base object in the hierarchy. Click Add Component in the Inspector panel, and search for and select LunarcomIntentRecognizer.

![Module4Chapter4step23im](images/module4chapter4step23im.PNG)

24. In the LUIS Endpoint field of the LunarcomIntentRecognizer in the inspector panel, enter the Endpoint URL that you saved in step 22. 

![Module4Chapter4step24im](images/module4chapter4step24im.PNG)

>  Note: In the LunarcomOfflineRecognizer component in the Inspector panel, make sure that Disable is selected for SimulateOfflineMode. Otherwise, testing the program will not work. 

25. Press the Play button in the Unity Editor, and click the rocket button to start intent recognition. Utter the phrase select the launch rocket button.

>  Note: The application recognized the desired function and activated the rocket button.
>
> ![Module4Chapter4step24im](images/module4chapter4note2im.PNG)

## Congratulations

You officially learned how to add speech commands from the speech SDK program, Now your program can recognize speech commands of all kinds of variants. Test it out and have a little fun with it.

[Next Lesson: Speech SDK Lesson 5](placeholderlink)

