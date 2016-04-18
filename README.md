# Slack Pokerbot for AWS Lambda

Pokerbot is a [Slash Command](https://api.slack.com/slash-commands) for [Slack](https://slack.com/). It's easily hosted on [Amazon Web Services' Lambda](https://aws.amazon.com/lambda/).

![Screenshot of Pokerbot in Slack](https://raw.githubusercontent.com/nateyolles/slack-pokerbot/master/images/screenshot.png)

## Configure Slack Slash Command

1. Navigate to https://<your-team-name>.slack.com/apps/manage/custom-integrations
2. Click on "Slash Commands" and "Add Configuration" 
3. Set the Command to "/pokerbot"
4. Set the URL to the path provided by AWS
5. Set the Method to "POST"
6. Set Custom Name to "pokerbot"
7. Customize Icon if you wish
8. Check "Show this command in the autocomplete list"
9. Set Description to "Play Scrum planning poker"
10. Set Usage hint to '"deal", "vote [0, 1, 2, 3, 5, 8, 13, 20]", "flip"'
11. Copy the Token

## Configure

1. Paste the Slack Token
2. Set the path to your images
3. Set the planning poker values you want to use (e.g. 0, 1, 2, 3, 5, 8, 13, 20, 40, 100)

## AWS Lambda

Follow instructions from Amazon Web Services Lambda. Paste the app.py file into the web editor or upload as directed by AWS.

## Play Poker Planning
1. Type "/pokerbot deal" in a channel
2. Everyone votes by typing "/pokerbot vote <your vote>"
3. Type "/pokerbot flip" in the channel to reveal the results
