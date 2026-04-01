<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>연애 스타일 테스트</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    body {
      margin: 0;
      overflow-x: hidden;
    }

    #confettiCanvas {
      position: fixed;
      inset: 0;
      z-index: 0;
      pointer-events: none;
      display: none;
    }

    .content-layer {
      position: relative;
      z-index: 1;
    }
  </style>
</head>
<body class="bg-pink-50 flex items-center justify-center min-h-screen p-4">

  <canvas id="confettiCanvas"></canvas>

  <div id="app" class="bg-white p-6 rounded-2xl shadow-xl w-full max-w-md text-center content-layer">
    <h1 class="text-2xl font-bold mb-4">💖 연애 스타일 테스트</h1>
    <div id="quiz"></div>
  </div>

  <script>
    const questions = [
      { q: "연인이 연락이 늦으면?", a: ["계속 기다린다", "조금 서운하지만 이해", "바로 연락함", "신경 안 씀"] },
      { q: "데이트 스타일은?", a: ["집 데이트", "카페", "액티비티", "여행"] },
      { q: "싸우면 어떻게 해?", a: ["먼저 사과", "대화로 해결", "시간을 둔다", "무시"] },
      { q: "애정 표현은?", a: ["말로", "행동으로", "선물", "자주 연락"] },
      { q: "이상형은?", a: ["다정", "재밌는", "성숙", "자유로운"] }
    ];

    let current = 0;
    let score = [0, 0, 0, 0];

    const app = document.getElementById("app");
    const canvas = document.getElementById("confettiCanvas");
    const ctx = canvas.getContext("2d");

    let pieces = [];
    let animationId = null;

    function getQuizElement() {
      return document.getElementById("quiz");
    }

    function showQuestion() {
      const quiz = getQuizElement();
      if (!quiz) return;

      const q = questions[current];

      quiz.innerHTML = `
        <p class="mb-4 text-lg font-medium">${q.q}</p>
        <div class="space-y-2">
          ${q.a.map((choice, i) => `
            <button
              data-index="${i}"
              class="choice-btn block w-full p-3 border rounded-lg hover:bg-pink-100 transition"
            >
              ${choice}
            </button>
          `).join("")}
        </div>
        <p class="mt-4 text-sm text-gray-500">${current + 1} / ${questions.length}</p>
      `;

      document.querySelectorAll(".choice-btn").forEach(btn => {
        btn.addEventListener("click", () => {
          const index = Number(btn.dataset.index);
          select(index);
        });
      });
    }

    function select(i) {
      score[i]++;
      current++;

      if (current < questions.length) {
        showQuestion();
      } else {
        showResult();
      }
    }

    function getResultData(max) {
      switch (max) {
        case 0:
          return {
            result: "💗 헌신형",
            match: "🔥 주도형",
            character: "재벌집 막내아들 - 진도준 (송중기)",
            desc: "상대를 오래 지켜보고 깊게 아끼는 타입입니다. 다만 참고만 있다가 감정이 쌓일 수 있습니다."
          };
        case 1:
          return {
            result: "💬 소통형",
            match: "💗 헌신형",
            character: "슬기로운 의사생활 - 안정원 (유연석)",
            desc: "대화와 공감을 중요하게 여기는 타입입니다. 관계를 풀어가는 힘이 강합니다."
          };
        case 2:
          return {
            result: "🔥 주도형",
            match: "💬 소통형",
            character: "이태원 클라쓰 - 박새로이 (박서준)",
            desc: "감정 표현이 분명하고 관계를 이끄는 힘이 있습니다. 다만 상대의 속도도 볼 필요가 있습니다."
          };
        case 3:
          return {
            result: "🌿 자유형",
            match: "💗 헌신형",
            character: "그 해 우리는 - 최웅 (최우식)",
            desc: "편안함과 자연스러움을 중시하는 타입입니다. 너무 무심하게 보이지 않도록만 주의하면 좋습니다."
          };
        default:
          return {
            result: "알 수 없음",
            match: "-",
            character: "-",
            desc: "-"
          };
      }
    }

    function showResult() {
      const max = score.indexOf(Math.max(...score));
      const { result, match, character, desc } = getResultData(max);

      document.body.className = "bg-black flex items-center justify-center min-h-screen p-4";
      app.className = "bg-zinc-900 text-white p-6 rounded-2xl shadow-2xl w-full max-w-md text-center content-layer";

      app.innerHTML = `
        <h1 class="text-3xl font-bold mb-4">🎉 결과 🎉</h1>
        <p class="mb-2 text-gray-300">당신의 연애 스타일</p>
        <p class="text-2xl font-bold mb-4">${result}</p>

        <p class="mb-2 text-gray-300">궁합이 좋은 스타일</p>
        <p class="text-xl font-semibold mb-4">${match}</p>

        <p class="mb-2 text-gray-300">추천 남주 스타일</p>
        <p class="text-lg mb-4">${character}</p>

        <div class="bg-white/10 rounded-xl p-4 mb-5 text-sm leading-relaxed text-gray-200">
          ${desc}
        </div>

        <button
          id="restartBtn"
          class="w-full bg-pink-500 hover:bg-pink-400 transition text-white font-semibold py-3 rounded-xl"
        >
          다시 테스트하기
        </button>
      `;

      startConfetti();

      document.getElementById("restartBtn").addEventListener("click", restartQuiz);
    }

    function restartQuiz() {
      stopConfetti();

      current = 0;
      score = [0, 0, 0, 0];

      document.body.className = "bg-pink-50 flex items-center justify-center min-h-screen p-4";
      app.className = "bg-white p-6 rounded-2xl shadow-xl w-full max-w-md text-center content-layer";

      app.innerHTML = `
        <h1 class="text-2xl font-bold mb-4">💖 연애 스타일 테스트</h1>
        <div id="quiz"></div>
      `;

      showQuestion();
    }

    function resizeCanvas() {
      canvas.width = window.innerWidth;
      canvas.height = window.innerHeight;
    }

    function createConfetti() {
      pieces = [];
      for (let i = 0; i < 160; i++) {
        pieces.push({
          x: Math.random() * canvas.width,
          y: Math.random() * canvas.height - canvas.height,
          r: Math.random() * 5 + 2,
          dx: (Math.random() - 0.5) * 2,
          dy: Math.random() * 3 + 2
        });
      }
    }

    function drawConfetti() {
      ctx.clearRect(0, 0, canvas.width, canvas.height);
      ctx.fillStyle = "white";

      for (const p of pieces) {
        ctx.beginPath();
        ctx.arc(p.x, p.y, p.r, 0, Math.PI * 2);
        ctx.fill();

        p.x += p.dx;
        p.y += p.dy;

        if (p.y > canvas.height + 10) {
          p.y = -10;
          p.x = Math.random() * canvas.width;
        }

        if (p.x < -10) p.x = canvas.width + 10;
        if (p.x > canvas.width + 10) p.x = -10;
      }

      animationId = requestAnimationFrame(drawConfetti);
    }

    function startConfetti() {
      canvas.style.display = "block";
      resizeCanvas();
      createConfetti();
      stopConfetti();
      canvas.style.display = "block";
      drawConfetti();
    }

    function stopConfetti() {
      if (animationId) {
        cancelAnimationFrame(animationId);
        animationId = null;
      }
      ctx.clearRect(0, 0, canvas.width, canvas.height);
      canvas.style.display = "none";
    }

    window.addEventListener("resize", resizeCanvas);

    showQuestion();
  </script>
</body>
</html>
