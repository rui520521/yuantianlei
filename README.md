<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <!-- 移动端适配关键标签 -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>袁天磊 - 个人简历</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: "Microsoft Yahei", sans-serif;
        }

        body {
            background-color: #f5f7fa;
            color: #333;
            line-height: 1.6;
        }

        .container {
            max-width: 900px;
            margin: 30px auto;
            background: #fff;
            padding: 40px;
            border-radius: 12px;
            box-shadow: 0 2px 15px rgba(0,0,0,0.1);
        }

        /* 头部信息 */
        .header {
            text-align: center;
            border-bottom: 2px solid #0066cc;
            padding-bottom: 20px;
            margin-bottom: 30px;
        }

        .header h1 {
            font-size: 2.2rem;
            color: #0066cc;
            margin-bottom: 10px;
        }

        .info-item {
            font-size: 1.1rem;
            margin: 6px 0;
        }

        /* 章节通用样式 */
        section {
            margin: 25px 0;
        }

        section h2 {
            border-left: 5px solid #0066cc;
            padding-left: 12px;
            font-size: 1.4rem;
            margin-bottom: 15px;
            color: #222;
        }

        ul {
            list-style-position: inside;
            padding-left: 10px;
        }

        li {
            margin: 8px 0;
            font-size: 1rem;
        }

        /* 按钮交互 */
        #toggleMore {
            padding: 10px 20px;
            background-color: #0066cc;
            color: white;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            margin-top: 15px;
            font-size: 1rem;
        }

        #toggleMore:hover {
            background-color: #0052a3;
        }

        .more-content {
            margin-top: 15px;
            display: none;
        }

        /* 移动端适配 */
        @media (max-width: 768px) {
            .container {
                margin: 15px;
                padding: 20px;
            }
            .header h1 {
                font-size: 1.8rem;
            }
            section h2 {
                font-size: 1.2rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- 头部个人信息 -->
        <div class="header">
            <h1>袁天磊</h1>
            <p class="info-item">学号：2025381044</p>
            <p class="info-item">求职意向：在校实习生 / 技术助理</p>
        </div>

        <!-- 教育经历 -->
        <section>
            <h2>教育背景</h2>
            <ul>
                <li>在读本科生 | 计算机相关专业</li>
                <li>在校时间：2025年9月 — 至今</li>
            </ul>
        </section>

        <!-- 专业技能 -->
        <section>
            <h2>专业技能</h2>
            <ul>
                <li>前端基础：HTML、CSS、原生JavaScript</li>
                <li>熟练制作响应式网页，适配移动端与PC端</li>
                <li>掌握基础网页布局、盒子模型、Flex布局</li>
                <li>能独立编写静态页面并实现简单交互效果</li>
            </ul>
        </section>

        <!-- 项目经验 -->
        <section>
            <h2>项目经验</h2>
            <ul>
                <li>个人简历静态网页开发（当前页面）</li>
                <li>实现响应式布局、JS点击展开效果</li>
            </ul>

            <button id="toggleMore">查看更多自我评价</button>
            <div class="more-content" id="selfEval">
                <ul>
                    <li>学习态度端正，动手能力强，善于钻研前端技术</li>
                    <li>做事认真负责，有良好的团队协作意识</li>
                    <li>能够持续自学新技术，按时完成开发任务</li>
                </ul>
            </div>
        </section>
    </div>

    <script>
        // 获取元素
        const btn = document.getElementById('toggleMore');
        const content = document.getElementById('selfEval');

        // 点击切换显示隐藏
        btn.addEventListener('click', function () {
            if (content.style.display === 'block') {
                content.style.display = 'none';
                btn.innerText = '查看更多自我评价';
            } else {
                content.style.display = 'block';
                btn.innerText = '收起内容';
            }
        });

        // 页面加载完成弹窗展示姓名学号
        window.onload = function () {
            alert("欢迎来到袁天磊的简历页面\n姓名：袁天磊\n学号：2025381044");
        }
    </script>
</body>
</html>
