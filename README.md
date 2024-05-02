
## Grafana and Copilot Metrics Dashboard

This is a personal project where I've developed a sample dashboard in Grafana Cloud to help teams and companies visualise GitHub copilot metrics within Grafana via the [Copilot API](https://docs.github.com/en/rest/copilot/copilot-usage?apiVersion=2022-11-28). Feel free to make suggestions in the Issues tab and get in contact via [Contact Info](#contact-info)



<img width="1255" alt="image" src="https://github.com/kleeadrian/Grafana-CopilotMetrics/assets/22606299/594b6b00-aa57-416b-9ba2-ed4f81b69cf3">



## How to get started with creating your dashboard!

### GitHub 
Login and create a [Personal access token](https://docs.github.com/en/enterprise-cloud@latest/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens) that will match the permission requirements for the [GitHub Copilot API](https://docs.github.com/en/rest/copilot/copilot-usage?apiVersion=2022-11-28#get-a-summary-of-copilot-usage-for-enterprise-members)
- [Click here for Enterprises Copilot API Endpoints requirements](https://docs.github.com/en/rest/copilot/copilot-usage?apiVersion=2022-11-28#get-a-summary-of-copilot-usage-for-enterprise-members)
- [Click here for Organisation Copilot API Endpoints requirements](https://docs.github.com/en/rest/copilot/copilot-usage?apiVersion=2022-11-28#get-a-summary-of-copilot-usage-for-organization-members)

Save the secret and don't expose it!

### Grafana
- Sign up for a [free Grafana Cloud account](https://grafana.com/auth/sign-up/create-user). You can have up to 3 free users!
- Follow the prompts and add your own cloud stack. Your Grafana Cloud stack URL should be XXXXXX.grafana.net
- Wait a couple of minutes and get ☕ or 🍵
- Navigate to your cloud stack URL and welcome to Grafana Cloud!!
- On the left hand side of the screen, go to the Add new connection button
<img width="236" alt="Screenshot 2024-05-02 at 6 45 31 pm" src="https://github.com/kleeadrian/Grafana-CopilotMetrics/assets/22606299/40cf8f43-2644-4804-9d69-910cf2a12dd8">

- Search for 'infinity' and click on the data source
<img width="336" alt="Screenshot 2024-05-02 at 6 45 45 pm" src="https://github.com/kleeadrian/Grafana-CopilotMetrics/assets/22606299/a83dc032-f1bf-4af7-82c6-9463dddd440c">

- Click on Install on the right hand corner. Wait 2 minutes and enjoy ☕

<img width="1720" alt="image" src="https://github.com/kleeadrian/Grafana-CopilotMetrics/assets/22606299/c1d5bf72-076d-4542-baf4-dfe7f507c915">

- Click on the left hand menu button in the top left hand corner and navigate to Data Sources

<img width="307" alt="image" src="https://github.com/kleeadrian/Grafana-CopilotMetrics/assets/22606299/f45e5fb1-0140-410a-a6fb-4c2fa4605e04">

- Click on add new Data Source
- Type in Infinity in the search bar and click on the infinity result. You should be at this page
<img width="1718" alt="image" src="https://github.com/kleeadrian/Grafana-CopilotMetrics/assets/22606299/3736ab6c-bb42-42d9-bf2f-5697153b9be4">

- Rename your data source name to whatever you like. Ideally 'GitHub Copilot'

- Click on the default flag to turn it on(optional)
- Go to the Authentication tab and paste your GitHub token in Bearer Token
- Add 'https://api.github.com' as allowed hosts
- Click Save and Test
- Navigate to the left hand menu ---> Dashboards ---> New ----> Import ----> Paste/Upload the copilotsample.json contents into the screen
- Select the Data source you created earlier
- VOILA! Your dashboard is here

**Note:** You'll need to change the URL of each panel to the specified API endpoints above. Do this by going to the top right hand corner of each Panel --> Edit --> change URL... or follow the instructions under the JSON template edit subheading

<img width="352" alt="image" src="https://github.com/kleeadrian/Grafana-CopilotMetrics/assets/22606299/1adb9bf5-5b06-4198-8dfb-e38ed1c9849a">

### Json template edits
The current .json file contains the template of the dashboard. It uses test sample data(same as the GitHub API response) which I've exported into a .json file which is located in the dummydata folder. 
The following lines of code are the ones that need to be changed to your Enterprise/Organisation API Endpoint

Change the URL's in the following lines to your [Organisation API Endpoint](https://docs.github.com/en/rest/copilot/copilot-user-management?apiVersion=2022-11-28)
```
162
413
```
Change the URL's in the following lines to your [Enterprise API Endpoint](https://docs.github.com/en/rest/copilot/copilot-usage?apiVersion=2022-11-28#get-a-summary-of-copilot-usage-for-enterprise-members)
```
254
536
685
831
998
1170
1290
```

Metrics ideas obtained from https://resources.github.com/learn/pathways/copilot/essentials/measuring-the-impact-of-github-copilot/ 

Shoutout to @andrekolodockha and @benksmilie for the ideas

# Contact Info
Feel free to contact me to discuss any issues, questions, or comments.

My contact info can be found on my GitHub page.





