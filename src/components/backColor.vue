<template>
    <div class="backColorDiv"></div>
</template>

<script>
    export default {
        name: 'BackColor',
        created: function () {
            if ('serviceWorker' in navigator) {
                navigator.serviceWorker && navigator.serviceWorker.register('../service-worker.js').then(() => {
                    //
                });
            }
            // 「弹出添加到主屏对话框」事件
            window.addEventListener('beforeinstallprompt', event => {
                // 这个 `event.userChoice` 是一个 Promise ，在用户选择后 resolve
                event.userChoice.then(result => {
                    console.log(result.outcome)
                    // 'accepted': 添加到主屏
                    // 'dismissed': 用户不想理你并向你扔了个取消
                })
            })
        }
    }
</script>

<style scoped>
    .backColorDiv {
        width: 100%;
        height: 100%;
        background: url("../../public/color.jpg") no-repeat 50% 50%;
    }
</style>