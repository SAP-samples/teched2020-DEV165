# Create Slack Instance

## Prerequisites 
- You have set up **Integration Suite** trial anad activated the **Open Connectors** capability. If you have not done this yet, refer to [Prerequisites](/exercises/Prerequisites/Prerequisites_for_DEV165.md) for detailed guidance.
- Ensure that you have logged into your **Slack** workspace in the same browser. Otherwise, the authentication experience will not be seamless.

1. Access your **Integration Suite Launchpad**.
![Access Integration Suite Launchpad](/exercises/Images/Launchpad/cockpit-access-launchpad.png)

2. Launch the **Open Connectors** capability.
![Launch OCN](/exercises/Images/Launchpad/launchpad-select-ocn.png)

3. Select the ***Connectors*** tab.
![Select Connectors Tab](/exercises/Images/OCN/ocn-select-connectors.png)

4. Filter for **Slack** and click on ***Authenticate***.
![Authenticate Slack Connector](/exercises/Images/Slack/ocn-authenticate-slack.png)

5. Provide a name for the instance and click on ***Create Instance***.
![Authenticate Slack Connector 1](/exercises/Images/Slack/ocn-authenticate-slack-1.png)

6. In a new browser tab, a confirmation dialog will open requesting you to allow access to your **Slack** channel. Please click on allow.
![Authenticate Slack Connector 2](/exercises/Images/Slack/ocn-authenticate-slack-2.png)

7. You will see a confirmation dialog that the instance has been created. Now, let us test it using the API docs that are provided out-of-the-box. Click on ***Test in the API Docs***. 
![Test Slack Connector 1](/exercises/Images/Slack/ocn-slack-testapidoc-1.png)

8. Look for the resource **/channels** with **POST** operation. This resource will let you create a new channel. Click on ***Try it out***.
![Test Slack Connector 1.1](/exercises/Images/Slack/ocn-slack-testapidoc-1.1.png)

9. In the **Edit Value** field, specify the channel name as **teched2020** and click on **Execute**.
![Test Slack Connector 1.2](/exercises/Images/Slack/ocn-slack-testapidoc-1.2.png)

  If the call is successful, you will seethe response code 200.

10. Access to your **Slack** account. You should see a new channel with the name **teched2020**.
![Test Slack Connector 1.3](/exercises/Images/Slack/ocn-slack-testapidoc-1.3.png)

11. Switch back to **Open Connectors**. In the **API Docs**, look for the resource **/channels/{channelId}/messages**. This resource will let you post a message to your Slack channel. Click on ***Try it out***.
![Test Slack Connector 2](/exercises/Images/Slack/ocn-slack-testapidoc-2.png)

12. You have to provide your **ChannelID**. This is the last part of the URL when you have accessed your Slack channel. Please copy and paste it in the ***channelid*** field. Enter a message in the same format as shown in the screenshot below and then click on ***Execute**.
![Test Slack Connector 3](/exercises/Images/Slack/ocn-slack-testapidoc-3.png)

13. If everything is in order, you will see a response code **200** indicating a successful operation. You will also see a message in your Slack channel, **My Test Message** or whatever text that you provided in the request body. 
![Test Slack Connector 4](/exercises/Images/Slack/ocn-slack-testapidoc-4.png)

You now have a working Slack **Open Connectors** instance. 
