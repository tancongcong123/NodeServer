创建微型服务器 nodejs express
1 npm init 
    是路径变成合法的包
2 npm i express
    安装express
3 开启服务器端口号5005 
    app.listen(5005, (error)=>{
    if(!error){
        console.log('服务器启动了');
    }
    })
4 app.use(express.static(__dirname+'/static'))
    配置路径
5 将前端生成的dist中的内容放到static文件夹中 重启服务器
6 访问http://localhost:5005/

ps 解决vue-router history模式打包页面刷新404问题
1 安装connect-history-api-fallback插件
    npm i connect-history-api-fallback
2 使用
    const history = require('connect-history-api-fallback')
    const app = express()
    app.use(history)