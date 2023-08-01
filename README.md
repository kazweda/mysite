# mysite
django tutorial mysite 
```
django-admin startproject mysite .
```

## モデルにメソッドを追加
```
def was_published_recently(self):
        return self.pub_date >= timezone.now() - datetime.timedelta(days=1)
```
