##Hello Trema
Hello Tremaが起動したら次のメッセージを表示するようにしてみよう
```
Hello Trema started.
```

##解答
サンプルプログラムの一部を以下のように変更した
```
  def start(_args)
    logger.info 'Trema started.'
  end
```

↓

```
  def start(_args)
    logger.info "#{self.class.name} started."
  end
```

self.class.nameを用いることによって自身のクラスを取得するようにした。
単純に名前を変えただけだと今後変更を加える際に手間となり拡張性に欠けるために、
このようにするとクラス名を変更するだけで済むので綺麗なコードになる。
