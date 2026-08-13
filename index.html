<!DOCTYPE html>
<html lang="ar" dir="rtl">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>ريمو AI</title>

    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            min-height: 100vh;
            font-family: Arial, Tahoma, sans-serif;

            background:
                radial-gradient(
                    circle at top right,
                    #202a4a 0%,
                    transparent 35%
                ),
                radial-gradient(
                    circle at bottom left,
                    #24163d 0%,
                    transparent 35%
                ),
                #080b12;

            color: white;

            display: flex;
            justify-content: center;
            align-items: center;

            padding: 20px;
        }

        .chat {
            width: 100%;
            max-width: 850px;
            height: 700px;

            background: rgba(17, 24, 39, 0.94);

            border: 1px solid rgba(255,255,255,0.08);

            border-radius: 24px;

            overflow: hidden;

            display: flex;
            flex-direction: column;

            box-shadow:
                0 30px 80px rgba(0,0,0,0.55);

            backdrop-filter: blur(20px);
        }

        /* HEADER */

        .header {
            height: 85px;

            padding: 18px 22px;

            background: rgba(255,255,255,0.03);

            border-bottom:
                1px solid rgba(255,255,255,0.07);

            display: flex;
            align-items: center;

            gap: 14px;
        }

        .avatar {
            width: 50px;
            height: 50px;

            border-radius: 50%;

            background:
                linear-gradient(
                    135deg,
                    #6366f1,
                    #8b5cf6
                );

            display: flex;
            justify-content: center;
            align-items: center;

            font-size: 22px;
            font-weight: bold;

            box-shadow:
                0 0 25px rgba(99,102,241,0.35);
        }

        .header h1 {
            font-size: 20px;
            margin-bottom: 5px;
        }

        .status {
            color: #22c55e;
            font-size: 13px;
        }

        /* MESSAGES */

        .messages {
            flex: 1;

            padding: 25px;

            overflow-y: auto;

            display: flex;
            flex-direction: column;

            gap: 15px;
        }

        .messages::-webkit-scrollbar {
            width: 6px;
        }

        .messages::-webkit-scrollbar-thumb {
            background: #374151;
            border-radius: 10px;
        }

        .message {
            max-width: 80%;

            padding: 14px 17px;

            border-radius: 18px;

            line-height: 1.8;

            white-space: pre-wrap;

            word-break: break-word;

            animation: messageIn 0.2s ease;
        }

        @keyframes messageIn {
            from {
                opacity: 0;
                transform: translateY(8px);
            }

            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .user {
            align-self: flex-start;

            background:
                linear-gradient(
                    135deg,
                    #4f46e5,
                    #6366f1
                );

            border-bottom-left-radius: 5px;
        }

        .remo {
            align-self: flex-end;

            background: #1b2433;

            border:
                1px solid rgba(255,255,255,0.07);

            border-bottom-right-radius: 5px;
        }

        .typing {
            opacity: 0.65;
        }

        /* INPUT */

        .input-area {
            padding: 18px;

            background: rgba(255,255,255,0.03);

            border-top:
                1px solid rgba(255,255,255,0.07);

            display: flex;

            gap: 10px;
        }

        #message {
            flex: 1;

            height: 52px;

            background: #0d1422;

            color: white;

            border:
                1px solid #303b50;

            border-radius: 15px;

            padding: 0 17px;

            outline: none;

            font-size: 15px;

            transition: 0.2s;
        }

        #message::placeholder {
            color: #6b7280;
        }

        #message:focus {
            border-color: #6366f1;

            box-shadow:
                0 0 0 3px
                rgba(99,102,241,0.12);
        }

        #sendBtn {
            height: 52px;

            min-width: 100px;

            border: none;

            border-radius: 15px;

            background:
                linear-gradient(
                    135deg,
                    #6366f1,
                    #7c3aed
                );

            color: white;

            cursor: pointer;

            font-size: 15px;

            font-weight: bold;

            transition: 0.2s;
        }

        #sendBtn:hover {
            transform: translateY(-1px);

            box-shadow:
                0 8px 25px
                rgba(99,102,241,0.25);
        }

        #sendBtn:disabled {
            opacity: 0.5;

            cursor: not-allowed;

            transform: none;

            box-shadow: none;
        }

        /* MOBILE */

        @media (max-width: 600px) {

            body {
                padding: 0;
            }

            .chat {
                height: 100vh;

                max-width: none;

                border-radius: 0;
            }

            .message {
                max-width: 90%;
            }

            .input-area {
                padding: 12px;
            }

            #sendBtn {
                min-width: 80px;
            }
        }
    </style>
</head>


<body>

<div class="chat">

    <!-- HEADER -->

    <div class="header">

        <div class="avatar">
            R
        </div>

        <div>

            <h1>
                ريمو AI
            </h1>

            <div
                class="status"
                id="status"
            >
                ● متصل
            </div>

        </div>

    </div>


    <!-- MESSAGES -->

    <div
        class="messages"
        id="messages"
    >

        <div class="message remo">

            أهلاً 👋

            أنا ريمو.

            اكتبلي أي حاجة وأنا هحاول أساعدك.

        </div>

    </div>


    <!-- INPUT -->

    <div class="input-area">

        <input
            type="text"
            id="message"
            placeholder="اكتب رسالتك لريمو..."
            autocomplete="off"
        >

        <button
            id="sendBtn"
            type="button"
        >
            إرسال
        </button>

    </div>

</div>


<script>

    /*
    ==================================================
    REMO API
    ==================================================
    */

    const API_URL =
        "https://sheet-corrections-famous-bar.trycloudflare.com                                    ";


    /*
    ==================================================
    LITELLM KEY

    ده مفتاح الاختبار المحلي بتاعك.
    لا ترفع نسخة تحتوي عليه إلى GitHub Public.
    ==================================================
    */

    const API_KEY =
        "sk-remo-2026";


    /*
    ==================================================
    MODEL
    ==================================================
    */

    const MODEL =
        "remo";


    /*
    ==================================================
    ELEMENTS
    ==================================================
    */

    const input =
        document.getElementById("message");

    const sendBtn =
        document.getElementById("sendBtn");

    const messages =
        document.getElementById("messages");

    const status =
        document.getElementById("status");


    /*
    ==================================================
    ADD MESSAGE
    ==================================================
    */

    function addMessage(text, type) {

        const message =
            document.createElement("div");

        message.className =
            "message " + type;

        message.textContent =
            text;

        messages.appendChild(message);

        messages.scrollTop =
            messages.scrollHeight;

        return message;
    }


    /*
    ==================================================
    ASK REMO
    ==================================================
    */

    async function askRemo(userMessage) {

        const response =
            await fetch(
                API_URL,
                {
                    method: "POST",

                    headers: {

                        "Content-Type":
                            "application/json",

                        "Authorization":
                            "Bearer " + API_KEY

                    },

                    body: JSON.stringify({

                        model: MODEL,

                        messages: [

                            {
                                role: "system",

                                content:
                                    `
أنت ريمو.

تحدث دائمًا باللغة العربية.

إذا تحدث المستخدم باللهجة المصرية،
تحدث معه باللهجة المصرية.

كن ذكيًا ومفيدًا ومباشرًا.

لا تخترع المعلومات.

إذا لم تكن متأكدًا من معلومة تقنية،
وضح أنك غير متأكد.
`
                            },

                            {
                                role: "user",

                                content:
                                    userMessage
                            }

                        ],

                        temperature: 0.3

                    })
                }
            );


        /*
        ==============================================
        CHECK RESPONSE
        ==============================================
        */

        if (!response.ok) {

            const errorText =
                await response.text();

            throw new Error(
                "HTTP " +
                response.status +
                " - " +
                errorText
            );
        }


        /*
        ==============================================
        JSON
        ==============================================
        */

        const data =
            await response.json();


        console.log(
            "REMO RESPONSE:",
            data
        );


        /*
        ==============================================
        GET ANSWER
        ==============================================
        */

        const answer =
            data
            ?.choices
            ?.at(0)
            ?.message
            ?.content;


        if (!answer) {

            throw new Error(
                "لم يصل رد صحيح من REMO"
            );
        }


        return answer;
    }


    /*
    ==================================================
    SEND MESSAGE
    ==================================================
    */

    async function sendMessage() {

        const text =
            input.value.trim();


        /*
        منع الرسالة الفارغة
        */

        if (!text) {
            return;
        }


        /*
        عرض رسالة المستخدم
        */

        addMessage(
            text,
            "user"
        );


        /*
        تفريغ Input
        */

        input.value = "";


        /*
        تعطيل الإرسال
        */

        sendBtn.disabled =
            true;


        /*
        حالة ريمو
        */

        status.textContent =
            "● ريمو بيفكر...";

        status.style.color =
            "#f59e0b";


        /*
        رسالة مؤقتة
        */

        const typing =
            addMessage(
                "ريمو بيفكر...",
                "remo typing"
            );


        try {

            /*
            إرسال إلى API
            */

            const answer =
                await askRemo(text);


            /*
            إزالة Thinking
            */

            typing.remove();


            /*
            عرض رد ريمو
            */

            addMessage(
                answer,
                "remo"
            );


            /*
            Connected
            */

            status.textContent =
                "● متصل";

            status.style.color =
                "#22c55e";

        }


        catch (error) {

            console.error(
                "REMO ERROR:",
                error
            );


            typing.remove();


            /*
            عرض الخطأ للمستخدم
            */

            addMessage(
                "حصل خطأ وأنا بحاول أوصل لريمو.\n\n" +
                "تأكد إن LiteLLM وCloudflare Tunnel شغالين.",
                "remo"
            );


            status.textContent =
                "● خطأ في الاتصال";

            status.style.color =
                "#ef4444";

        }


        /*
        إعادة تفعيل الزر
        */

        sendBtn.disabled =
            false;


        /*
        التركيز على Input
        */

        input.focus();

    }


    /*
    ==================================================
    SEND BUTTON
    ==================================================
    */

    sendBtn.addEventListener(
        "click",
        sendMessage
    );


    /*
    ==================================================
    ENTER
    ==================================================
    */

    input.addEventListener(
        "keydown",
        function(event) {

            if (
                event.key === "Enter"
            ) {

                event.preventDefault();

                sendMessage();

            }

        }
    );


    /*
    ==================================================
    FOCUS
    ==================================================
    */

    input.focus();

</script>

</body>

</html>
