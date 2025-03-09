<!DOCTYPE html>
<html lang="zh">
<head>
    <meta charset="UTF-8">
    <title>HTML中的时钟</title>
    <style>
        /* 简单的样式 */
        #clock {
            font-size: 2em;
            font-family: Arial, sans-serif;
            color: #333;
            text-align: center;
            margin-top: 20%;
        }
    </style>
</head>
<body>

<div id="clock"></div>

<script>
    function updateClock() {
        const now = new Date(); // 获取当前时间
        let hours = now.getHours().toString().padStart(2, '0'); // 小时
        let minutes = now.getMinutes().toString().padStart(2, '0'); // 分钟
        let seconds = now.getSeconds().toString().padStart(2, '0'); // 秒

        // 更新页面上的时钟
        document.getElementById('clock').textContent = `${hours}:${minutes}:${seconds}`;

        // 使用setTimeout每秒调用一次updateClock函数
        setTimeout(updateClock, 1000);
    }

    // 页面加载完成后开始执行
    window.onload = function() {
        updateClock();
    };
</script>

</body>
</html>
