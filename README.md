<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Vocabulary Practice - iron, whole, switched on, how did it go, dry, payslip, how about, up to</title>
    <style>
        :root {
            --primary: #64d404;
            --primary-dark: #2f9e44;
            --accent: #22c1c3;
            --bg: #f4f9f4;
            --card-bg: #ffffff;
            --text-main: #123029;
            --text-muted: #5f6b6d;
            --error: #e03131;
            --success: #2f9e44;
            --radius-lg: 16px;
            --radius-xl: 22px;
            --shadow-soft: 0 10px 25px rgba(0,0,0,0.08);
        }

        * {
            box-sizing: border-box;
        }

        body {
            margin: 0;
            font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
            background: linear-gradient(135deg, #e9f9ec, #f0fffb);
            color: var(--text-main);
        }

        .app-container {
            max-width: 1100px;
            margin: 24px auto 40px;
            padding: 0 16px;
        }

        header {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
            gap: 12px;
            margin-bottom: 16px;
        }

        .title-block {
            display: flex;
            flex-direction: column;
            gap: 4px;
        }

        h1 {
            margin: 0;
            font-size: 1.8rem;
            background: linear-gradient(135deg, #168aad, #2f9e44);
            -webkit-background-clip: text;
            color: transparent;
        }

        .subtitle {
            margin: 0;
            font-size: 0.95rem;
            color: var(--text-muted);
        }

        .score-badge {
            margin-left: auto;
            padding: 8px 16px;
            border-radius: 999px;
            background: linear-gradient(135deg, rgba(100,212,4,0.1), rgba(34,193,195,0.1));
            border: 1px solid rgba(100,212,4,0.3);
            font-weight: 600;
            font-size: 0.95rem;
            color: var(--primary-dark);
            box-shadow: 0 4px 12px rgba(0,0,0,0.04);
            white-space: nowrap;
        }

        .nav-buttons {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 18px;
        }

        .nav-button {
            border: none;
            padding: 8px 14px;
            border-radius: 999px;
            font-size: 0.9rem;
            cursor: pointer;
            background: rgba(255,255,255,0.8);
            color: var(--text-main);
            box-shadow: 0 4px 12px rgba(0,0,0,0.04);
            transition: all 0.15s ease;
        }

        .nav-button:hover {
            transform: translateY(-1px);
            box-shadow: 0 7px 18px rgba(0,0,0,0.08);
        }

        .nav-button.active {
            background: linear-gradient(135deg, var(--primary), var(--accent));
            color: #ffffff;
        }

        main {
            background: rgba(255,255,255,0.9);
            border-radius: var(--radius-xl);
            box-shadow: var(--shadow-soft);
            padding: 18px 18px 22px;
        }

        section {
            display: none;
        }

        section.active {
            display: block;
        }

        .section-title {
            margin-top: 0;
            margin-bottom: 6px;
            font-size: 1.25rem;
        }

        .section-subtitle {
            margin: 0 0 14px;
            font-size: 0.9rem;
            color: var(--text-muted);
        }

        .vocab-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 12px;
        }

        .vocab-card {
            background: var(--card-bg);
            border-radius: var(--radius-lg);
            padding: 12px 13px;
            box-shadow: 0 4px 14px rgba(0,0,0,0.04);
            border: 1px solid rgba(22,138,173,0.08);
            display: flex;
            flex-direction: column;
            gap: 4px;
        }

        .vocab-word-row {
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 6px;
        }

        .vocab-word {
            font-weight: 700;
            font-size: 1.05rem;
        }

        .context-pill {
            display: inline-flex;
            align-items: center;
            padding: 2px 8px;
            border-radius: 999px;
            background: rgba(34,193,195,0.08);
            font-size: 0.78rem;
            color: var(--text-muted);
        }

        .vocab-meaning {
            font-size: 0.9rem;
            color: var(--text-main);
        }

        .vocab-example {
            font-size: 0.85rem;
            color: var(--text-muted);
        }

        .hear-button {
            border: none;
            border-radius: 999px;
            padding: 4px 10px;
            font-size: 0.8rem;
            cursor: pointer;
            background: linear-gradient(135deg, var(--primary), var(--accent));
            color: #ffffff;
            display: inline-flex;
            align-items: center;
            gap: 4px;
        }

        .hear-button span {
            font-size: 0.85rem;
        }

        .word-bank {
            margin: 10px 0 14px;
            padding: 8px 10px;
            border-radius: 14px;
            background: linear-gradient(135deg, rgba(100,212,4,0.9), rgba(34,193,195,0.95));
            color: #ffffff;
            font-size: 0.86rem;
            box-shadow: 0 8px 18px rgba(0,0,0,0.18);
        }

        .word-bank-title {
            font-weight: 600;
            margin-bottom: 4px;
        }

        .word-chip {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: 2px 9px;
            border-radius: 999px;
            background: rgba(255,255,255,0.18);
            margin: 2px 4px 0 0;
            font-size: 0.8rem;
        }

        .exercise-list {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .exercise-item {
            background: var(--card-bg);
            border-radius: var(--radius-lg);
            padding: 10px 11px;
            box-shadow: 0 4px 14px rgba(0,0,0,0.03);
            border: 1px solid rgba(0,0,0,0.03);
        }

        .exercise-sentence {
            font-size: 0.92rem;
            margin-bottom: 6px;
        }

        .gap-input {
            padding: 4px 6px;
            border-radius: 999px;
            border: 1px solid rgba(0,0,0,0.16);
            font-size: 0.9rem;
            min-width: 110px;
        }

        .gap-input.correct {
            border-color: var(--success);
            background: #ebfbee;
        }

        .gap-input.incorrect {
            border-color: var(--error);
            background: #fff5f5;
        }

        .feedback {
            font-size: 0.8rem;
            color: var(--text-muted);
        }

        .feedback.success {
            color: var(--success);
        }

        .feedback.error {
            color: var(--error);
        }

        .button-row {
            margin-top: 10px;
            display: flex;
            gap: 8px;
        }

        .primary-btn, .secondary-btn {
            border-radius: 999px;
            padding: 7px 14px;
            font-size: 0.85rem;
            cursor: pointer;
            border: none;
            display: inline-flex;
            align-items: center;
            gap: 6px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.06);
        }

        .primary-btn {
            background: linear-gradient(135deg, var(--primary), var(--accent));
            color: #ffffff;
        }

        .secondary-btn {
            background: #f1f3f5;
            color: var(--text-main);
        }

        .primary-btn:hover,
        .secondary-btn:hover {
            transform: translateY(-1px);
            box-shadow: 0 7px 18px rgba(0,0,0,0.09);
        }

        .match-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 12px;
        }

        .match-column {
            background: var(--card-bg);
            border-radius: var(--radius-lg);
            padding: 10px 11px;
            box-shadow: 0 4px 14px rgba(0,0,0,0.03);
            border: 1px solid rgba(0,0,0,0.03);
        }

        .match-column-title {
            font-size: 0.9rem;
            font-weight: 600;
            margin-bottom: 8px;
        }

        .match-item-btn {
            width: 100%;
            text-align: left;
            border-radius: 999px;
            border: 1px solid rgba(0,0,0,0.12);
            padding: 6px 10px;
            margin-bottom: 6px;
            font-size: 0.85rem;
            background: #ffffff;
            cursor: pointer;
            transition: all 0.12s ease;
        }

        .match-item-btn:hover {
            background: #f1f3f5;
        }

        .match-item-btn.selected {
            border-color: var(--accent);
            background: rgba(34,193,195,0.1);
        }

        .match-item-btn.correct {
            background: #ebfbee;
            border-color: var(--success);
            color: var(--success);
            cursor: default;
        }

        .match-item-btn.disabled {
            pointer-events: none;
            opacity: 0.7;
        }

        .match-feedback {
            margin-top: 6px;
            font-size: 0.82rem;
            color: var(--text-muted);
        }

        .mic-button {
            border-radius: 999px;
            border: none;
            padding: 4px 9px;
            font-size: 0.82rem;
            cursor: pointer;
            background: linear-gradient(135deg, #22c1c3, #64d404);
            color: #ffffff;
            display: inline-flex;
            align-items: center;
            gap: 4px;
        }

        .mic-button.disabled {
            background: #dee2e6;
            color: #868e96;
            cursor: not-allowed;
        }

        .blank-placeholder {
            display: inline-block;
            min-width: 80px;
            border-bottom: 2px dashed rgba(0,0,0,0.35);
            text-align: center;
            padding: 1px 2px;
        }

        .blank-placeholder.filled {
            border-bottom-color: transparent;
            font-weight: 600;
            color: var(--success);
        }

        .pron-support-warning {
            font-size: 0.85rem;
            color: var(--error);
            margin-bottom: 6px;
        }

        @media (max-width: 700px) {
            header {
                flex-direction: column;
                align-items: flex-start;
            }

            .score-badge {
                margin-left: 0;
            }

            main {
                padding: 14px;
            }
        }
    </style>
</head>
<body>
<div class="app-container">
    <header>
        <div class="title-block">
            <h1>Vocabulary Trainer</h1>
            <p class="subtitle">Practice writing, meaning, and pronunciation with interactive exercises.</p>
        </div>
        <div class="score-badge" id="scoreDisplay">Score: 0 / 24</div>
    </header>

    <div class="nav-buttons">
        <button class="nav-button active" data-target="vocabSection">📚 Vocabulary List</button>
        <button class="nav-button" data-target="writingSection">✍️ Fill in the Gaps (Writing)</button>
        <button class="nav-button" data-target="matchSection">🔗 Match Definitions</button>
        <button class="nav-button" data-target="pronSection">🎤 Pronunciation Gaps</button>
    </div>

    <main>
        <section id="vocabSection" class="active">
            <h2 class="section-title">Vocabulary List</h2>
            <p class="section-subtitle">Review the words, their meanings, and example sentences. Click ▶️ to hear each word or expression.</p>
            <div class="vocab-list" id="vocabList"></div>
        </section>

        <section id="writingSection">
            <h2 class="section-title">Fill in the Gaps (Writing)</h2>
            <p class="section-subtitle">Type the correct word or expression from the word bank into each sentence.</p>
            <div class="word-bank" id="writingWordBank">
                <div class="word-bank-title">Word Bank</div>
                <div id="writingWords"></div>
            </div>
            <div class="exercise-list" id="writingExercises"></div>
            <div class="button-row">
                <button class="primary-btn" id="checkWritingBtn">✅ Check Answers</button>
                <button class="secondary-btn" id="resetWritingBtn">🔄 Reset Inputs</button>
            </div>
        </section>

        <section id="matchSection">
            <h2 class="section-title">Match Definitions</h2>
            <p class="section-subtitle">Click a word or expression and then the definition that matches it.</p>
            <div class="match-container">
                <div class="match-column">
                    <div class="match-column-title">Words / Expressions</div>
                    <div id="matchWords"></div>
                </div>
                <div class="match-column">
                    <div class="match-column-title">Definitions</div>
                    <div id="matchDefinitions"></div>
                </div>
            </div>
            <div class="match-feedback" id="matchFeedback"></div>
        </section>

        <section id="pronSection">
            <h2 class="section-title">Fill in the Gaps (Pronunciation)</h2>
            <p class="section-subtitle">Say the missing word or expression. If it is recognized correctly, the blank will be filled in.</p>
            <div id="pronSupportMsg" class="pron-support-warning" style="display:none;">
                Speech recognition is not supported in this browser. The microphone activities may not work.
            </div>
            <div class="word-bank">
                <div class="word-bank-title">Word Bank</div>
                <div id="pronWords"></div>
            </div>
            <div class="exercise-list" id="pronExercises"></div>
        </section>
    </main>
</div>

<script>
    // Vocabulary data
    const vocabItems = [
        {
            word: "iron",
            context: "as stirare (to iron clothes)",
            meaning: "to make clothes smooth by moving a hot iron over them",
            example: "She needs to iron her shirt before the job interview.",
            writingSentence: "He woke up early to __ his trousers so they looked neat for work.",
            pronSentence: "After washing the clothes, she will __ the shirts and hang them in the wardrobe.",
            definition: "to press clothes with a hot iron to make them smooth"
        },
        {
            word: "whole",
            context: "",
            meaning: "all of something; complete, not divided into parts",
            example: "He ate the whole pizza by himself.",
            writingSentence: "They spent the __ day at the beach, from morning until sunset.",
            pronSentence: "She read the __ book in just two evenings.",
            definition: "all of something; complete, not just a part"
        },
        {
            word: "switched on",
            context: "as clever and smart; mentally alert and quick to understand",
            meaning: "very aware, quick to understand things, and generally clever and smart",
            example: "The new manager is really switched on and understands the problems of the team quickly.",
            writingSentence: "You need to be __ in this job because things change very fast.",
            pronSentence: "The students in this class are very __ and ask thoughtful questions.",
            definition: "very alert and aware, and generally clever and quick to understand things"
        },
        {
            word: "how did it go",
            context: "fixed expression: asking about the result or experience",
            meaning: "a phrase used to ask someone about the result or experience of something",
            example: "When he came back from the interview, his friends immediately asked, \"How did it go?\"",
            writingSentence: "After your driving test, your friend will probably ask, \"__?\"",
            pronSentence: "When she returned from the meeting, her colleague smiled and said, \"So, __?\"",
            definition: "a question you ask to find out how an event, exam, or situation went"
        },
        {
            word: "dry",
            context: "",
            meaning: "not wet or without water or other liquid",
            example: "Hang the clothes outside so they can get dry in the sun.",
            writingSentence: "Make sure the floor is __ before you walk on it, or you might slip.",
            pronSentence: "The towels are finally __ after spending hours in the dryer.",
            definition: "not wet; without water or other liquid"
        },
        {
            word: "payslip",
            context: "as busta paga",
            meaning: "a document given to an employee showing how much they have been paid and the amounts taken for tax etc.",
            example: "She checked her payslip to make sure the overtime was included.",
            writingSentence: "Your __ shows your salary, tax, and any other deductions for the month.",
            pronSentence: "He keeps every __ in a folder so he can check his income at the end of the year.",
            definition: "a document that shows how much salary you received and what was deducted"
        },
        {
            word: "how about",
            context: "as che ne dici se",
            meaning: "a phrase used to make a suggestion or ask for an opinion about an idea",
            example: "How about going for a walk after dinner?",
            writingSentence: "We could stay at home, or __ going out for a pizza instead?",
            pronSentence: "If you are bored, __ playing a board game together?",
            definition: "a phrase used to suggest something or ask what someone thinks of an idea"
        },
        {
            word: "up to",
            context: "as I can carry up to 10kg (maximum limit)",
            meaning: "no more than a particular number or amount; as much as but not more than",
            example: "This bus can carry up to fifty passengers.",
            writingSentence: "The suitcase must weigh __ 20 kilos, or you will have to pay extra.",
            pronSentence: "Members can borrow __ five books from the library at one time.",
            definition: "as much as but not more than a certain number or amount"
        }
    ];

    const totalPoints = vocabItems.length * 3;
    let currentScore = 0;
    document.getElementById("scoreDisplay").textContent = `Score: ${currentScore} / ${totalPoints}`;

    // Flags for scoring
    vocabItems.forEach(item => {
        item.writingCorrect = false;
        item.matchCorrect = false;
        item.pronCorrect = false;
    });

    function updateScoreDisplay() {
        document.getElementById("scoreDisplay").textContent = `Score: ${currentScore} / ${totalPoints}`;
    }

    function incrementScoreOnce(item, key) {
        if (!item[key]) {
            item[key] = true;
            currentScore += 1;
            updateScoreDisplay();
        }
    }

    // Utility: shuffle array
    function shuffleArray(arr) {
        const a = arr.slice();
        for (let i = a.length - 1; i > 0; i--) {
            const j = Math.floor(Math.random() * (i + 1));
            [a[i], a[j]] = [a[j], a[i]];
        }
        return a;
    }

    // Navigation
    const navButtons = document.querySelectorAll(".nav-button");
    const sections = document.querySelectorAll("main section");

    navButtons.forEach(btn => {
        btn.addEventListener("click", () => {
            const target = btn.getAttribute("data-target");
            navButtons.forEach(b => b.classList.remove("active"));
            btn.classList.add("active");
            sections.forEach(sec => {
                if (sec.id === target) sec.classList.add("active");
                else sec.classList.remove("active");
            });
        });
    });

    // Speech synthesis
    function speak(word) {
        if (!("speechSynthesis" in window)) {
            alert("Speech synthesis is not supported in this browser.");
            return;
        }
        const u = new SpeechSynthesisUtterance(word);
        u.lang = "en-US";
        speechSynthesis.speak(u);
    }
    window.speak = speak;

    // Build Vocabulary List
    function buildVocabList() {
        const container = document.getElementById("vocabList");
        vocabItems.forEach(item => {
            const card = document.createElement("div");
            card.className = "vocab-card";

            const topRow = document.createElement("div");
            topRow.className = "vocab-word-row";

            const wordEl = document.createElement("div");
            wordEl.className = "vocab-word";
            wordEl.textContent = item.word;

            const hearBtn = document.createElement("button");
            hearBtn.className = "hear-button";
            hearBtn.type = "button";
            hearBtn.innerHTML = `<span>▶️</span><span>Hear</span>`;
            hearBtn.addEventListener("click", () => speak(item.word));

            topRow.appendChild(wordEl);
            topRow.appendChild(hearBtn);
            card.appendChild(topRow);

            if (item.context && item.context.trim() !== "") {
                const ctx = document.createElement("div");
                ctx.className = "context-pill";
                ctx.textContent = `Context: ${item.context}`;
                card.appendChild(ctx);
            }

            const meaningEl = document.createElement("div");
            meaningEl.className = "vocab-meaning";
            meaningEl.textContent = item.meaning;
            card.appendChild(meaningEl);

            const exampleEl = document.createElement("div");
            exampleEl.className = "vocab-example";
            exampleEl.textContent = "Example: " + item.example;
            card.appendChild(exampleEl);

            container.appendChild(card);
        });
    }

    // Build Writing Section
    function buildWritingSection() {
        const wordBank = document.getElementById("writingWords");
        vocabItems.forEach(item => {
            const chip = document.createElement("span");
            chip.className = "word-chip";
            chip.textContent = item.word;
            wordBank.appendChild(chip);
        });

        const exercisesContainer = document.getElementById("writingExercises");
        const shuffled = shuffleArray(vocabItems);

        shuffled.forEach((item, index) => {
            const ex = document.createElement("div");
            ex.className = "exercise-item";

            const sent = document.createElement("div");
            sent.className = "exercise-sentence";

            const parts = item.writingSentence.split("__");
            const before = parts[0] || "";
            const after = parts[1] || "";

            const spanBefore = document.createElement("span");
            spanBefore.textContent = before;

            const input = document.createElement("input");
            input.type = "text";
            input.className = "gap-input";
            input.setAttribute("data-word", item.word);
            input.setAttribute("data-index", index.toString());

            const spanAfter = document.createElement("span");
            spanAfter.textContent = after;

            sent.appendChild(spanBefore);
            sent.appendChild(input);
            sent.appendChild(spanAfter);

            const fb = document.createElement("div");
            fb.className = "feedback";
            fb.id = `writing-feedback-${index}`;

            ex.appendChild(sent);
            ex.appendChild(fb);
            exercisesContainer.appendChild(ex);
        });

        document.getElementById("checkWritingBtn").addEventListener("click", () => {
            const inputs = exercisesContainer.querySelectorAll(".gap-input");
            inputs.forEach(input => {
                const expected = input.getAttribute("data-word");
                const index = input.getAttribute("data-index");
                const fb = document.getElementById(`writing-feedback-${index}`);
                const userVal = (input.value || "").trim().toLowerCase();
                const target = (expected || "").toLowerCase();

                input.classList.remove("correct", "incorrect");
                fb.classList.remove("success", "error");

                if (!expected) return;

                if (userVal === target) {
                    input.classList.add("correct");
                    fb.classList.add("success");
                    fb.textContent = "✅ Correct!";
                    const item = vocabItems.find(v => v.word === expected);
                    if (item) incrementScoreOnce(item, "writingCorrect");
                } else if (userVal.length > 0) {
                    input.classList.add("incorrect");
                    fb.classList.add("error");
                    fb.textContent = "❌ Try again.";
                } else {
                    fb.textContent = "✏️ Type a word or expression from the word bank.";
                }
            });
        });

        document.getElementById("resetWritingBtn").addEventListener("click", () => {
            const inputs = exercisesContainer.querySelectorAll(".gap-input");
            inputs.forEach(input => {
                input.value = "";
                input.classList.remove("correct", "incorrect");
            });
            const feedbacks = exercisesContainer.querySelectorAll(".feedback");
            feedbacks.forEach(fb => {
                fb.textContent = "";
                fb.classList.remove("success", "error");
            });
        });
    }

    // Match Definitions Section
    let selectedWordBtn = null;
    let selectedDefBtn = null;

    function buildMatchSection() {
        const wordsContainer = document.getElementById("matchWords");
        const defsContainer = document.getElementById("matchDefinitions");
        const feedback = document.getElementById("matchFeedback");

        const shuffledWords = shuffleArray(vocabItems);
        const defsArr = vocabItems.map(item => ({ word: item.word, definition: item.definition }));
        const shuffledDefs = shuffleArray(defsArr);

        shuffledWords.forEach(item => {
            const btn = document.createElement("button");
            btn.type = "button";
            btn.className = "match-item-btn";
            btn.textContent = item.word;
            btn.setAttribute("data-word", item.word);

            btn.addEventListener("click", () => {
                if (btn.classList.contains("correct")) return;
                if (selectedWordBtn === btn) {
                    btn.classList.remove("selected");
                    selectedWordBtn = null;
                } else {
                    if (selectedWordBtn) selectedWordBtn.classList.remove("selected");
                    selectedWordBtn = btn;
                    btn.classList.add("selected");
                }
                feedback.textContent = "";
                feedback.style.color = "#5f6b6d";
            });

            wordsContainer.appendChild(btn);
        });

        shuffledDefs.forEach((obj, idx) => {
            const btn = document.createElement("button");
            btn.type = "button";
            btn.className = "match-item-btn";
            btn.textContent = obj.definition;
            btn.setAttribute("data-word", obj.word);
            btn.setAttribute("data-index", idx.toString());

            btn.addEventListener("click", () => {
                if (btn.classList.contains("correct")) return;
                if (!selectedWordBtn) {
                    feedback.textContent = "👉 First, click a word or expression in the left column.";
                    feedback.style.color = "#5f6b6d";
                    return;
                }
                if (selectedDefBtn === btn) {
                    btn.classList.remove("selected");
                    selectedDefBtn = null;
                } else {
                    if (selectedDefBtn) selectedDefBtn.classList.remove("selected");
                    selectedDefBtn = btn;
                    btn.classList.add("selected");
                }

                const word = selectedWordBtn.getAttribute("data-word");
                const defWord = btn.getAttribute("data-word");

                if (word && defWord && word === defWord) {
                    selectedWordBtn.classList.add("correct", "disabled");
                    btn.classList.add("correct", "disabled");
                    selectedWordBtn.classList.remove("selected");
                    btn.classList.remove("selected");
                    feedback.textContent = "✅ Good match!";
                    feedback.style.color = "#2f9e44";
                    const item = vocabItems.find(v => v.word === word);
                    if (item) incrementScoreOnce(item, "matchCorrect");
                    selectedWordBtn = null;
                    selectedDefBtn = null;
                } else if (word && defWord) {
                    feedback.textContent = "❌ That definition does not match this item. Try again.";
                    feedback.style.color = "#e03131";
                    setTimeout(() => {
                        feedback.textContent = "";
                        feedback.style.color = "#5f6b6d";
                    }, 1500);
                    if (selectedWordBtn) selectedWordBtn.classList.remove("selected");
                    if (selectedDefBtn) selectedDefBtn.classList.remove("selected");
                    selectedWordBtn = null;
                    selectedDefBtn = null;
                }
            });

            defsContainer.appendChild(btn);
        });
    }

    // Pronunciation Section
    let recognition = null;
    let recognitionAvailable = false;
    let currentPronItem = null;

    function setupRecognition() {
        if ("webkitSpeechRecognition" in window) {
            recognition = new webkitSpeechRecognition();
        } else if ("SpeechRecognition" in window) {
            recognition = new SpeechRecognition();
        } else {
            recognition = null;
        }

        if (recognition) {
            recognition.lang = "en-US";
            recognition.interimResults = false;
            recognition.maxAlternatives = 1;
            recognitionAvailable = true;
        } else {
            recognitionAvailable = false;
            const msg = document.getElementById("pronSupportMsg");
            if (msg) msg.style.display = "block";
        }
    }

    function normalizeText(text) {
        return (text || "").toLowerCase().trim().replace(/\s+/g, "");
    }

    function buildPronSection() {
        const wordBank = document.getElementById("pronWords");
        vocabItems.forEach(item => {
            const chip = document.createElement("span");
            chip.className = "word-chip";
            chip.textContent = item.word;
            wordBank.appendChild(chip);
        });

        const container = document.getElementById("pronExercises");
        const shuffled = shuffleArray(vocabItems);

        shuffled.forEach((item, idx) => {
            const ex = document.createElement("div");
            ex.className = "exercise-item";

            const sent = document.createElement("div");
            sent.className = "exercise-sentence";

            const parts = item.pronSentence.split("__");
            const before = parts[0] || "";
            const after = parts[1] || "";

            const spanBefore = document.createElement("span");
            spanBefore.textContent = before;

            const blank = document.createElement("span");
            blank.className = "blank-placeholder";
            blank.textContent = "___";
            blank.setAttribute("data-word", item.word);
            blank.setAttribute("data-index", idx.toString());
            blank.id = `pron-blank-${idx}`;

            const spanAfter = document.createElement("span");
            spanAfter.textContent = after;

            sent.appendChild(spanBefore);
            sent.appendChild(blank);
            sent.appendChild(spanAfter);

            const controls = document.createElement("div");
            controls.style.display = "flex";
            controls.style.alignItems = "center";
            controls.style.gap = "8px";
            controls.style.marginTop = "6px";

            const micBtn = document.createElement("button");
            micBtn.type = "button";
            micBtn.className = "mic-button";
            micBtn.innerHTML = "🎙️ Say the word";
            micBtn.setAttribute("data-word", item.word);
            micBtn.setAttribute("data-index", idx.toString());
            micBtn.id = `pron-mic-${idx}`;

            const fb = document.createElement("div");
            fb.className = "feedback";
            fb.id = `pron-feedback-${idx}`;

            if (!recognitionAvailable) {
                micBtn.classList.add("disabled");
                micBtn.disabled = true;
            }

            micBtn.addEventListener("click", () => {
                if (!recognitionAvailable || !recognition) {
                    fb.textContent = "Speech recognition is not available in this browser.";
                    fb.classList.add("error");
                    return;
                }
                if (item.pronCorrect) {
                    fb.textContent = "✅ This item has already been recognized correctly.";
                    fb.classList.add("success");
                    return;
                }
                currentPronItem = { item, index: idx, expected: item.word };

                fb.textContent = "🎧 Listening... Please say the word or expression clearly.";
                fb.classList.remove("error", "success");

                recognition.start();
            });

            controls.appendChild(micBtn);
            controls.appendChild(fb);

            ex.appendChild(sent);
            ex.appendChild(controls);
            container.appendChild(ex);
        });

        if (recognition) {
            recognition.onresult = (event) => {
                if (!currentPronItem) return;
                const transcript = event.results[0][0].transcript;
                const heard = normalizeText(transcript);
                const expected = normalizeText(currentPronItem.expected);
                const idx = currentPronItem.index;

                const fb = document.getElementById(`pron-feedback-${idx}`);
                const blank = document.getElementById(`pron-blank-${idx}`);

                if (heard === expected) {
                    fb.textContent = `✅ Recognized: "${currentPronItem.item.word}"`;
                    fb.classList.remove("error");
                    fb.classList.add("success");

                    if (blank) {
                        blank.textContent = currentPronItem.item.word;
                        blank.classList.add("filled");
                    }

                    incrementScoreOnce(currentPronItem.item, "pronCorrect");
                } else {
                    fb.textContent = `❌ Heard "${transcript}". Try again.`;
                    fb.classList.remove("success");
                    fb.classList.add("error");
                }

                currentPronItem = null;
            };

            recognition.onerror = () => {
                if (currentPronItem) {
                    const idx = currentPronItem.index;
                    const fb = document.getElementById(`pron-feedback-${idx}`);
                    if (fb) {
                        fb.textContent = "⚠️ There was a problem with recognition. Please try again.";
                        fb.classList.add("error");
                    }
                    currentPronItem = null;
                }
            };

            recognition.onend = () => {
                // Ready for next attempt
            };
        }
    }

    // Init
    document.addEventListener("DOMContentLoaded", () => {
        setupRecognition();
        buildVocabList();
        buildWritingSection();
        buildMatchSection();
        buildPronSection();
    });
</script>
</body>
</html>
