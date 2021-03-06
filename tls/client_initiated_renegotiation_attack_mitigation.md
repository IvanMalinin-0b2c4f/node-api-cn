
<!-- type=misc -->

TLS 协议允许客户端在 TLS 会话中进行重协商，用于安全因素的考量。
不幸的是，会话重协商需要消耗大量的服务器端资源，这将导致服务器存在潜在的被 DDoS 攻击的可能。

为了减轻这个风险，限制每十分钟只能使用三次重协商，超过这个限制将会在 [`tls.TLSSocket`] 实例中产生一个 `error` 事件。
这个限制是可配置的:

* `tls.CLIENT_RENEG_LIMIT` {number} 指定重协商请求的次数限制，默认为 `3`。
* `tls.CLIENT_RENEG_WINDOW` {number} 指定限制次数的生效时间段，默认为 `600`（10 分钟）。

不应在未充分理解其含义与影响的情况下修改上述参数。

TLSv1.3 不支持重协商。

