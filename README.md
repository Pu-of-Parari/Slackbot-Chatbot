# Slackbot-Chatbot

- Chatbot on Slack using seq2seq model
- About the model implementation, refer to [here](https://github.com/Pu-of-Parari/Japanese-Neural-Conversational-Model).

# 0.Setup
This scripts is implemented by Python3 and TensorFlow v0.12.

`pip install -r requirements.txt`


And please create a bot account on Slack. (you can get[ here](https://mychatbottalk.slack.com/apps/new/yA0F7YS25R-bots))
This scripts use the `API_TOKEN`

# 1.Setting


```
slackbot
    ├ data_utils.py
    ├ data
    |  ├ checkpoint                               
    |  ├ translate.ckpt-xxxx.data-00000-of-00001  
    |  ├ translate.ckpt-xxxx.index                
    |  ├ vocab_in.txt                             
    |  └ vocab_out.txt
    |
    ├ seq2seq_model.py
    |
    ├ run.py                 #botを起動するためのメインスクリプト
    ├ slackbot_settings.py   #bot設定用スクリプト
    └ plugins
        ├ __init__.py        
        └ my_mention.py      #seq2seqによるデコードを応答に用いる
                              ためのスクリプト
```

Put your model and `vocab` file on `/data`.
About `slackbot_settings.py`, it is necessary to change to your own `API_TOKEN`.

# 2. Run
Executing `run.py`

`python run.py`

You can chat with bot after the bot account on slack comes online. Enjoy :)

<br>

![screenshot](https://github.com/Pu-of-Parari/Slackbot-Chatbot/blob/master/slackbot.png)
