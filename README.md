# mysite
django tutorial mysite 
```
django-admin startproject mysite .
```

## __str__
自動生成adminでオブジェクトの表現として使用される。
```
def __str__(self):
    return self.question_text
```

## モデルにメソッドを追加
```
def was_published_recently(self):
    return self.pub_date >= timezone.now() - datetime.timedelta(days=1)
```

## アプリをadminに登録
```
from .models import Question

admin.site.register(Question)
```

## 簡単なフォーム
polls/templates/polls/detail.html

question.idでvoteのURLへPOST

選択肢(choice)のset.all()でループを回して
inputタグを生成する。

vote(request, question_id)の処理は views.py へ記述する。

投票結果を results.html で表示する。
