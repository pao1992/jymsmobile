<template>
    <div>
        <p>{{data}}</p>
        <ul v-if="dataHasLoaded">
            <li>引擎版本信息: {{ver}}</li>
            <li>系统类型: {{sType}}</li>
            <li>系统版本: {{sVer}}</li>
            <li>设备标识: {{id}}</li>
            <li>设备型号: {{model}}</li>
            <li>设备名称: {{name}}</li>
            <li>网络状态: {{cType}}</li>
            <li>主窗口名字: {{winName}}</li>
            <li>主窗口宽度: {{winWidth}}</li>
            <li>主窗口高度: {{winHeight}}</li>
            <li>子窗口名字: {{frameName}}</li>
            <li>子窗口宽度: {{frameWidth}}</li>
            <li>子窗口高度: {{frameHeight}}</li>
        </ul>
    </div>
</template>

<script>


    export default {
        data() {
            return {
                data:'原始数据',
                dataHasLoaded: false,
            }
        },
        created() {
            this.ver = api.version;
            this.sType = api.systemType;
            this.sVer = api.systemVersion;
            this.id = api.deviceId;
            this.model = api.deviceModel;
            this.name = api.deviceName;
            this.cType = api.connectionType;
            this.winName = api.winName;
            this.winWidth = api.winWidth;
            this.winHeight = api.winHeight;
            this.frameName = api.frameName || '';
            this.frameWidth = api.frameWidth || '';
            this.frameHeight = api.frameHeight || '';
            this.dataHasLoaded = true;
            this.initData()
        },
        methods: {
            initData(){
//                var that = this;
//                ajpush.init(function(ret, err){
//                    if(ret && ret.status){
//                        alert('操作成功!');
//                    }else{
//                        alert('操作失败!');
//                    }
//                });
//                ajpush.setListener(
//                        function(ret) {
//                            var id = ret.id;
//                            var title = ret.title;
//                            var content = ret.content;
//                            var extra = ret.extra;
//                            that.data = id+title+content;
//                        }
//                );
//                ajpush.getRegistrationId(function(ret) {
//                    var registrationId = ret.id;
//                    console.log(registrationId)
//                });
//                ajpush.stopPush(function(ret) {
//                    if(ret && ret.status){
//                        console.log('停止发送')
//                    }
//                });
//                ajpush.isPushStopped(function(ret) {
//                    if(ret && ret.isStopped){
//                        console.log('服务已停止')
//                    }
//                });
//                ajpush.resumePush(function(ret) {
//                    if(ret && ret.status){
//                        console.log('恢复发送')
//                        //success
//                    }
//                });
//                api.addEventListener({name:'resume'}, function(ret,err) {
//                    console.log('恢复到前台');
//                    ajpush.onResume();
//                });
//                api.addEventListener({name:'pause'}, function(ret,err) {
//                    console.log('切换到后台');
//                    ajpush.onPause();
//                });
////                ajpush.setListener(
////                        function(ret) {
//////                            var id = ret.id;
//////                            var title = ret.title;
//////                            var content = ret.content;
//////                            var extra = ret.extra;
////                            that.data = ret.id+'/'+ret.content
////                            console.log(that.data)
////                        }
////                );
//                ajpush.removeListener();

            },
            getPush(){

            },
            onPause(){

            },
            onResume(){

            }
        }
    }
</script>
