# PomeloClientForCocosCreate

导入为插件：

var pomelo = window.pomelo;
var host = "127.0.0.1";
var port = "3010";
var self = this;
pomelo.init({
    host: host,
    port: port,
    log: true
}, function() {
    pomelo.request("connector.entryHandler.entry", "hello pomelo", function(data) {
        self.label.string = data.msg;
    });
});
