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
