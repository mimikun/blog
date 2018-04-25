+++
title = "Mastodonをはじめて1年が経ちました"
date = "2018-04-26T01:17:36+09:00"
draft = false
description = ""
tags = []
categories = []
images = []
banner = ""
menu = ""
+++

# Mastodonを初めて一年経ちました。
ぼくがJP鯖こと[mstdn.jp](https://mstdn.jp)にアカウントを作成したのは2017/04/16らしいのでもう1年は経ってることになります。

## アカウントのcreated_at(ながいので注意)
ちゃーんと1年経っています。

**"created_at": "2017-04-16T12:26:23.443Z"**

```
$ curl -X POST -Ss https://${MASTODON_HOST}/api/v1/statuses \
--header "Authorization: Bearer ${ACCESS_TOKEN}" \
-d "status=${STATUS}" | python -m json.tool

{
    "id": "99921131215047720",
    "created_at": "2018-04-25T16:57:44.108Z",
    "in_reply_to_id": null,
    "in_reply_to_account_id": null,
    "sensitive": false,
    "spoiler_text": "",
    "visibility": "public",
    "language": "ja",
    "uri": "https://mstdn.jp/users/mimikun/statuses/99921131215047720",
    "content": "<p>test</p>",
    "url": "https://mstdn.jp/@mimikun/99921131215047720",
    "reblogs_count": 0,
    "favourites_count": 0,
    "favourited": false,
    "reblogged": false,
    "muted": false,
    "pinned": false,
    "reblog": null,
    "application": {
        "name": "created_at\u898b\u308b\u3084\u3064",
        "website": ""
    },
    "account": {
        "id": "63705",
        "username": "mimikun",
        "acct": "mimikun",
        "display_name": "mimikun@JP",
        "locked": false,
        "created_at": "2017-04-16T12:26:23.443Z",
        "note": "<p>\u8266\u3053\u308c\u3068\u304b\u30d7\u30ed\u30b0\u30e9\u30df\u30f3\u30b0\u3068\u304b\u97f3\u30b2\u30fc\u3068\u304b<br />\u81ea\u9bd6: <a href=\"https://mstdn.mimikun.jp/@mimikun\" rel=\"nofollow noopener\" target=\"_blank\"><span class=\"invisible\">https://</span><span class=\"\">mstdn.mimikun.jp/@mimikun</span><span class=\"invisible\"></span></a></p>",
        "url": "https://mstdn.jp/@mimikun",
        "avatar": "https://media.mstdn.jp/images/accounts/avatars/000/063/705/original/79281f93a06105d3.jpeg",
        "avatar_static": "https://media.mstdn.jp/images/accounts/avatars/000/063/705/original/79281f93a06105d3.jpeg",
        "header": "https://mstdn.jp/headers/original/missing.png",
        "header_static": "https://mstdn.jp/headers/original/missing.png",
        "followers_count": 23,
        "following_count": 10,
        "statuses_count": 135
    },
    "media_attachments": [],
    "mentions": [],
    "tags": [],
    "emojis": []
}
```

## Mastodonはじめて思ったこと
- **Twitterの代わりにはならない**

MastodonはTwitterの代わりにはならないです。

でもTwitterには無い連合やローカルタイムライン(LTL)という仕組みがあるので繋がりを増やすことはそんなに難しくなかったです。

~~あとはユーザ検索さえなんとかなればなー。。。~~

## 最後に
書いてて色々アレになったのでこれの続きは自分のインスタンスこと[mimikun丼](https://mstdn.mimikun.jp)が一年経ったらかくとおもいます。~~多分な！！！~~
