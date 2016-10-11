##スイッチ切断のイベント
仮想スイッチを停止したら、コントローラで次のメッセージを表示するようにしてみよう
```
Bye 0xabc
```

##解答
サンプルプログラムに以下のコードを追加した

```
  def switch_disconnected(datapath_id)
    logger.info "Bye #{datapath_id.to_hex}"
  end
```

switch_disconnectedを用いて、切断時に切断されたスイッチを表示するようにした。

別の端末で
```
trema stop 0xabc
```
を実行し正しく動いているのを確認した。
