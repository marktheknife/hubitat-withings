# hubitat-withings
This integration provides you with a way to integrate your various Withings devices into Hubitat using their official API. Currently this supports scales, thermometers, activity trackers, blood pressure monitors, and sleep pads. You will need to obtain API access from Withings to set this up.

## Withings API
To obtain access to the Withings API, follow the steps below:
* Go to [https://account.withings.com/partner/add_oauth2](https://account.withings.com/partner/add_oauth2)
* Enter a Description, Contact Email, and Company name
* Enter **https://cloud.hubitat.com/oauth/stateredirect** for the Callback URL
* Choose **Prod** for the environment
* For the logo you can use **https://github.com/dcmeglio/hubitat-withings/raw/master/hubitat-logo.PNG**
* Note both the **Client Id** and **Consumer Secret**

## Configuration
Enter both the Client Id and Consumer Secret from above in the Withings Integration app. Click Done to install the app and reopen it. You can now add child apps for each of your Withings users. You will need to complete the OAuth steps in the app for each user. For each child app, make sure you choose a different user. Each device you choose will be created specific to the user. For example, if you have User1 and User1 and a Body Cardio Scale you will end up with two devices, *User1 Body Cardio* and *User2 Body Cardio*. As a result, devices that are shared (like scales) should be added under the child app for each user. Note that the Withings Sleep Sensor currently does not report a sleep status, only a status of when you get in/out of bed so this integration can NOT be used to detect when someone falls asleep. Hopefully they add this to the API in the future!

## Donations
If you find this app useful, please consider making a [donation](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=7LBRPJRLJSDDN&source=url)! 

## License
 Licensed Virtual the Apache License, Version 2.0 (the "License"); you may not use this file except
 in compliance with the License. You may obtain a copy of the License at:

 http://www.apache.org/licenses/LICENSE-2.0
 
 Unless required by applicable law or agreed to in writing, software distributed under the License is distributed
 on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License
 for the specific language governing permissions and limitations under the License.
