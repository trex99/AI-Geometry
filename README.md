<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Geometry of Intelligence: AI & Math Distance (2015-2025)</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Chart.js -->
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <!-- Plotly.js -->
    <script src="https://cdn.plot.ly/plotly-2.27.0.min.js"></script>

    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        bgDark: '#0f172a', // Slate 900
                        cardDark: '#1e293b', // Slate 800
                        primary: '#06b6d4', // Cyan 500
                        secondary: '#8b5cf6', // Violet 500
                        accent: '#f43f5e', // Rose 500
                        success: '#10b981', // Emerald 500
                        textMain: '#f8fafc', // Slate 50
                        textMuted: '#94a3b8', // Slate 400
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    }
                }
            }
        }
    </script>

    <style>
        body {
            background-color: #0f172a; /* bgDark */
            color: #f8fafc; /* textMain */
            font-family: 'Inter', sans-serif;
        }

        /* Chart Container Rules */
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 600px;
            height: 350px; /* Base height */
            max-height: 400px;
            margin-left: auto;
            margin-right: auto;
        }
        
        @media (min-width: 768px) {
            .chart-container {
                height: 400px;
            }
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #1e293b; 
        }
        ::-webkit-scrollbar-thumb {
            background: #475569; 
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #64748b; 
        }

        /* Timeline Connector */
        .timeline-line::before {
            content: '';
            position: absolute;
            top: 0;
            bottom: 0;
            left: 50%;
            width: 2px;
            background-color: #334155;
            transform: translateX(-50%);
            z-index: 0;
        }
    </style>
    <!-- 
        Palette Used: "Cyberpunk/Neon"
        Background: #0f172a (Deep Slate)
        Card: #1e293b (Lighter Slate)
        Accents: Cyan (#06b6d4), Violet (#8b5cf6), Rose (#f43f5e)
        Text: White/Grey
        
        Source Material Analysis:
        The content is based on the report "AI Learning & Mathematical Distance Concepts (2015-2025)".
        - Section 1: Intro
        - Section 2: Timeline (HTML List)
        - Section 3: WGAN (Line Chart - Compare)
        - Section 4: Embeddings (3D Scatter - Relationships)
        - Section 5: Attention (Bubble Chart - Relationships)
        - Section 6: Robustness (Radar Chart - Compare)
        - Section 7: Future (Doughnut - Composition)
        
        NO SVG USED. NO MERMAID USED.
    -->
</head>
<body class="antialiased selection:bg-primary selection:text-white">

    <!-- Navbar -->
    <nav class="sticky top-0 z-50 bg-bgDark/90 backdrop-blur-md border-b border-gray-800 shadow-lg">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-16">
                <div class="flex items-center">
                    <span class="text-2xl font-bold bg-clip-text text-transparent bg-gradient-to-r from-primary to-secondary">
                        AI Geometry
                    </span>
                </div>
                <div class="hidden md:block">
                    <div class="ml-10 flex items-baseline space-x-4">
                        <a href="#timeline" class="hover:text-primary px-3 py-2 rounded-md text-sm font-medium transition">Timeline</a>
                        <a href="#generative" class="hover:text-primary px-3 py-2 rounded-md text-sm font-medium transition">Generative</a>
                        <a href="#representation" class="hover:text-primary px-3 py-2 rounded-md text-sm font-medium transition">Embeddings</a>
                        <a href="#nlp" class="hover:text-primary px-3 py-2 rounded-md text-sm font-medium transition">NLP</a>
                        <a href="#robustness" class="hover:text-primary px-3 py-2 rounded-md text-sm font-medium transition">Robustness</a>
                    </div>
                </div>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <header class="relative overflow-hidden bg-gradient-to-b from-bgDark to-cardDark py-16 sm:py-24">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10 text-center">
            <h1 class="text-4xl sm:text-6xl font-extrabold tracking-tight text-white mb-6">
                The Geometry of <br>
                <span class="text-transparent bg-clip-text bg-gradient-to-r from-primary via-secondary to-accent">Artificial Intelligence</span>
            </h1>
            <p class="mt-4 max-w-2xl mx-auto text-xl text-textMuted">
                Analyzing the evolution of mathematical distance concepts in AI research (2015–2025). 
                From Euclidean space to Optimal Transport and Non-Euclidean geometry.
            </p>
            <div class="mt-10 flex justify-center gap-4">
                <div class="flex flex-col items-center p-4 bg-cardDark rounded-lg border border-gray-700 shadow-lg">
                    <span class="text-3xl font-bold text-primary">4</span>
                    <span class="text-sm text-textMuted uppercase tracking-wide">Key Metrics</span>
                </div>
                <div class="flex flex-col items-center p-4 bg-cardDark rounded-lg border border-gray-700 shadow-lg">
                    <span class="text-3xl font-bold text-secondary">2017</span>
                    <span class="text-sm text-textMuted uppercase tracking-wide">Transformer Era</span>
                </div>
                <div class="flex flex-col items-center p-4 bg-cardDark rounded-lg border border-gray-700 shadow-lg">
                    <span class="text-3xl font-bold text-accent">WGAN</span>
                    <span class="text-sm text-textMuted uppercase tracking-wide">Stability Shift</span>
                </div>
            </div>
        </div>
    </header>

    <main class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12 space-y-24">

        <!-- SECTION 1: Timeline -->
        <section id="timeline">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold text-white mb-4">Evolution of Distance (2015-2025)</h2>
                <p class="text-textMuted max-w-3xl mx-auto">
                    A decade of redefining "similarity." The field moved from simple pixel differences to deep semantic understanding and probability distributions.
                </p>
            </div>

            <div class="relative timeline-line max-w-4xl mx-auto">
                <!-- 2015 -->
                <div class="relative z-10 mb-8 flex justify-between items-center w-full flex-row-reverse left-timeline">
                    <div class="order-1 w-5/12"></div>
                    <div class="z-20 flex items-center order-1 bg-primary shadow-xl w-12 h-12 rounded-full justify-center font-bold text-bgDark">
                        '15
                    </div>
                    <div class="order-1 bg-cardDark rounded-lg shadow-xl w-5/12 px-6 py-4 border-l-4 border-primary">
                        <h3 class="font-bold text-white text-lg">Metric Learning & Adversarial Attacks</h3>
                        <p class="text-sm text-textMuted mt-1">
                            <span class="text-primary font-semibold">FaceNet</span> uses Triplet Loss (Euclidean).
                            <span class="text-accent font-semibold">FGSM</span> exploits L-infinity norm for attacks.
                        </p>
                    </div>
                </div>

                <!-- 2017 -->
                <div class="relative z-10 mb-8 flex justify-between items-center w-full">
                    <div class="order-1 w-5/12"></div>
                    <div class="z-20 flex items-center order-1 bg-secondary shadow-xl w-12 h-12 rounded-full justify-center font-bold text-white">
                        '17
                    </div>
                    <div class="order-1 bg-cardDark rounded-lg shadow-xl w-5/12 px-6 py-4 border-r-4 border-secondary text-right">
                        <h3 class="font-bold text-white text-lg">Optimal Transport & Attention</h3>
                        <p class="text-sm text-textMuted mt-1">
                            <span class="text-secondary font-semibold">Wasserstein GAN</span> solves gradient vanishing.
                            <span class="text-white font-semibold">Transformers</span> use Dot Product as semantic distance.
                        </p>
                    </div>
                </div>

                <!-- 2020 -->
                <div class="relative z-10 mb-8 flex justify-between items-center w-full flex-row-reverse left-timeline">
                    <div class="order-1 w-5/12"></div>
                    <div class="z-20 flex items-center order-1 bg-success shadow-xl w-12 h-12 rounded-full justify-center font-bold text-bgDark">
                        '20
                    </div>
                    <div class="order-1 bg-cardDark rounded-lg shadow-xl w-5/12 px-6 py-4 border-l-4 border-success">
                        <h3 class="font-bold text-white text-lg">Contrastive Learning</h3>
                        <p class="text-sm text-textMuted mt-1">
                            <span class="text-success font-semibold">SimCLR</span> & Supervised Contrastive Learning.
                            Maximizing Cosine Similarity between augmented views.
                        </p>
                    </div>
                </div>

                <!-- 2024+ -->
                <div class="relative z-10 mb-8 flex justify-between items-center w-full">
                    <div class="order-1 w-5/12"></div>
                    <div class="z-20 flex items-center order-1 bg-accent shadow-xl w-12 h-12 rounded-full justify-center font-bold text-white">
                        '25
                    </div>
                    <div class="order-1 bg-cardDark rounded-lg shadow-xl w-5/12 px-6 py-4 border-r-4 border-accent text-right">
                        <h3 class="font-bold text-white text-lg">Non-Euclidean & Semantic</h3>
                        <p class="text-sm text-textMuted mt-1">
                            Hyperbolic embeddings, Diffusion (KL divergence), and Semantic Distance in LLMs to reduce hallucinations.
                        </p>
                    </div>
                </div>
            </div>
        </section>

        <!-- SECTION 2: Wasserstein GAN (Line Chart) -->
        <section id="generative" class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
            <div class="order-2 md:order-1">
                <div class="chart-container bg-cardDark rounded-xl p-4 shadow-lg border border-gray-700">
                    <canvas id="wganChart"></canvas>
                </div>
            </div>
            <div class="order-1 md:order-2">
                <div class="inline-block px-3 py-1 mb-4 text-xs font-semibold tracking-wider text-secondary uppercase bg-secondary/10 rounded-full">
                    Probability Distributions
                </div>
                <h2 class="text-3xl font-bold text-white mb-4">Wasserstein Distance: Solving Stability</h2>
                <p class="text-textMuted mb-6 leading-relaxed">
                    Traditional GANs used Jensen-Shannon divergence, leading to vanishing gradients when distributions didn't overlap. 
                    <br><br>
                    The introduction of <strong>Earth Mover's Distance (Wasserstein)</strong> provided a smooth gradient everywhere, enabling stable training even when the generated distribution is far from the real one.
                </p>
                <ul class="space-y-3">
                    <li class="flex items-start">
                        <span class="flex-shrink-0 w-6 h-6 flex items-center justify-center rounded-full bg-secondary/20 text-secondary mr-3 font-bold text-sm">✓</span>
                        <span class="text-gray-300 text-sm">Replaced binary classification with regression of "critic" scores.</span>
                    </li>
                    <li class="flex items-start">
                        <span class="flex-shrink-0 w-6 h-6 flex items-center justify-center rounded-full bg-secondary/20 text-secondary mr-3 font-bold text-sm">✓</span>
                        <span class="text-gray-300 text-sm">Enforced 1-Lipschitz continuity via Gradient Penalty (WGAN-GP).</span>
                    </li>
                </ul>
            </div>
        </section>

        <!-- SECTION 3: Representation Learning (Plotly 3D) -->
        <section id="representation" class="bg-cardDark rounded-2xl p-8 shadow-2xl border border-gray-700">
            <div class="text-center mb-8">
                <div class="inline-block px-3 py-1 mb-4 text-xs font-semibold tracking-wider text-success uppercase bg-success/10 rounded-full">
                    Metric Learning
                </div>
                <h2 class="text-3xl font-bold text-white">Contrastive Embeddings (SimCLR)</h2>
                <p class="text-textMuted mt-2 max-w-2xl mx-auto">
                    Learning representations by pulling similar images (positives) closer and pushing different ones (negatives) apart using Cosine Similarity in a hypersphere.
                </p>
            </div>
            
            <!-- Full width chart container for Plotly -->
            <div class="w-full h-[500px] bg-bgDark rounded-xl overflow-hidden relative" id="plotly3d"></div>
            <p class="text-center text-xs text-textMuted mt-4 italic">
                *Conceptual visualization of 3D feature space after Contrastive Learning. Colors represent distinct classes.
            </p>
        </section>

        <!-- SECTION 4: NLP & Attention (Bubble Chart) -->
        <section id="nlp" class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
            <div>
                <div class="inline-block px-3 py-1 mb-4 text-xs font-semibold tracking-wider text-primary uppercase bg-primary/10 rounded-full">
                    Vector Space
                </div>
                <h2 class="text-3xl font-bold text-white mb-4">Attention is (Dot Product) Distance</h2>
                <p class="text-textMuted mb-6 leading-relaxed">
                    In Transformers (like BERT and GPT), the "relationship" between words is calculated using the <strong>Scaled Dot-Product Attention</strong>.
                    <br><br>
                    High dot products indicate high similarity (close semantic distance), allowing the model to focus on relevant context regardless of the positional distance in the sentence.
                </p>
                <div class="bg-bgDark p-6 rounded-lg border border-gray-700">
                    <h4 class="text-white font-semibold mb-2">Formulaic Logic:</h4>
                    <p class="font-mono text-sm text-primary">
                        Attention(Q, K, V) = softmax( (Q · Kᵀ) / √d ) V
                    </p>
                    <p class="text-xs text-textMuted mt-2">
                        The dot product (Q·K) measures the alignment between the Query and the Key.
                    </p>
                </div>
            </div>
            <div>
                <div class="chart-container bg-cardDark rounded-xl p-4 shadow-lg border border-gray-700">
                    <canvas id="attentionChart"></canvas>
                </div>
            </div>
        </section>

        <!-- SECTION 5: Robustness (Radar Chart) -->
        <section id="robustness">
            <div class="bg-gradient-to-br from-cardDark to-bgDark rounded-2xl p-8 border border-gray-700">
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
                    <div class="flex flex-col justify-center">
                        <div class="inline-block px-3 py-1 mb-4 text-xs font-semibold tracking-wider text-accent uppercase bg-accent/10 rounded-full w-fit">
                            Adversarial Defense
                        </div>
                        <h2 class="text-3xl font-bold text-white mb-4">Robustness via Lp Norms</h2>
                        <p class="text-textMuted mb-6">
                            Adversarial attacks (like FGSM, PGD) try to find a perturbation vector <em>delta</em> within a specific distance ball (L-infinity, L2) that maximizes loss.
                        </p>
                        <p class="text-textMuted mb-6">
                            Models trained with PGD (Projected Gradient Descent) show higher robustness against these distance-constrained attacks compared to standard training.
                        </p>
                    </div>
                    <div>
                        <div class="chart-container bg-bgDark rounded-xl p-4 shadow-lg border border-gray-700">
                            <canvas id="radarChart"></canvas>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- SECTION 6: Future Trends (Doughnut) -->
        <section id="future" class="py-12">
            <h2 class="text-3xl font-bold text-white text-center mb-12">2025 Outlook: The Next Metric</h2>
            
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-5xl mx-auto">
                <!-- Chart -->
                <div class="chart-container bg-cardDark rounded-xl p-4 shadow-lg border border-gray-700 flex justify-center items-center">
                    <canvas id="trendChart"></canvas>
                </div>

                <!-- Cards -->
                <div class="grid grid-cols-1 gap-4">
                    <div class="bg-cardDark p-6 rounded-lg border-l-4 border-secondary shadow-md hover:translate-x-2 transition-transform duration-300">
                        <h4 class="font-bold text-white text-lg">Hyperbolic Geometry</h4>
                        <p class="text-sm text-textMuted mt-2">
                            Using non-Euclidean spaces to better represent hierarchical data (e.g., taxonomies, code syntax trees) with fewer dimensions.
                        </p>
                    </div>
                    <div class="bg-cardDark p-6 rounded-lg border-l-4 border-success shadow-md hover:translate-x-2 transition-transform duration-300">
                        <h4 class="font-bold text-white text-lg">Semantic Consistency</h4>
                        <p class="text-sm text-textMuted mt-2">
                            Measuring "hallucination distance" in LLMs. Ensuring generated facts remain within a truth-bounded semantic region.
                        </p>
                    </div>
                    <div class="bg-cardDark p-6 rounded-lg border-l-4 border-primary shadow-md hover:translate-x-2 transition-transform duration-300">
                        <h4 class="font-bold text-white text-lg">Diffusion Metrics</h4>
                        <p class="text-sm text-textMuted mt-2">
                            Leveraging Fisher Divergence and score matching for high-fidelity image and video generation.
                        </p>
                    </div>
                </div>
            </div>
        </section>

    </main>

    <footer class="bg-bgDark border-t border-gray-800 py-12">
        <div class="max-w-7xl mx-auto px-4 text-center">
            <p class="text-textMuted text-sm">
                Generated by Canvas Infographics &bull; Data Source: AI Distance Metrics Analysis Report (2015-2025)
            </p>
            <p class="text-xs text-gray-600 mt-2">
                This infographic uses Chart.js and Plotly.js for visualization. No SVG files were used.
            </p>
        </div>
    </footer>

    <!-- SCRIPTS -->
    <script>
        // --- UTILITY: Label Wrapping ---
        function processLabels(labels) {
            const MAX_LENGTH = 16;
            return labels.map(label => {
                if (label.length <= MAX_LENGTH) return label;
                const words = label.split(' ');
                const lines = [];
                let currentLine = words[0];

                for (let i = 1; i < words.length; i++) {
                    if ((currentLine + " " + words[i]).length <= MAX_LENGTH) {
                        currentLine += " " + words[i];
                    } else {
                        lines.push(currentLine);
                        currentLine = words[i];
                    }
                }
                lines.push(currentLine);
                return lines;
            });
        }

        // --- UTILITY: Tooltip Configuration ---
        const commonTooltipOptions = {
            backgroundColor: 'rgba(15, 23, 42, 0.9)',
            titleColor: '#f8fafc',
            bodyColor: '#94a3b8',
            borderColor: '#334155',
            borderWidth: 1,
            padding: 10,
            callbacks: {
                title: function(tooltipItems) {
                    const item = tooltipItems[0];
                    let label = item.chart.data.labels[item.dataIndex];
                    if (Array.isArray(label)) {
                        return label.join(' ');
                    } else {
                        return label;
                    }
                }
            }
        };

        const commonChartOptions = {
            responsive: true,
            maintainAspectRatio: false,
            plugins: {
                legend: {
                    labels: { color: '#94a3b8', font: { family: 'Inter' } }
                },
                tooltip: commonTooltipOptions
            },
            scales: {
                x: {
                    grid: { color: '#334155' },
                    ticks: { color: '#94a3b8' }
                },
                y: {
                    grid: { color: '#334155' },
                    ticks: { color: '#94a3b8' }
                }
            }
        };

        // --- CHART 1: WGAN vs GAN (Line Chart) ---
        const ctxWgan = document.getElementById('wganChart').getContext('2d');
        const epochs = Array.from({length: 20}, (_, i) => i + 1);
        
        // Simulating: GAN (Erratic) vs WGAN (Smooth)
        const ganLoss = [8, 2, 7, 1, 9, 3, 6, 2, 8, 4, 1, 10, 2, 5, 8, 1, 9, 2, 7, 3];
        const wganLoss = [8, 7.5, 7, 6.5, 6, 5.6, 5.2, 4.8, 4.5, 4.2, 3.9, 3.7, 3.5, 3.3, 3.1, 3.0, 2.9, 2.8, 2.7, 2.6];

        new Chart(ctxWgan, {
            type: 'line',
            data: {
                labels: processLabels(epochs.map(e => `Epoch ${e}`)),
                datasets: [
                    {
                        label: 'Standard GAN (JS Div)',
                        data: ganLoss,
                        borderColor: '#f43f5e', // Accent Red
                        backgroundColor: 'rgba(244, 63, 94, 0.1)',
                        borderWidth: 2,
                        tension: 0.1,
                        pointRadius: 2
                    },
                    {
                        label: 'WGAN (Wasserstein)',
                        data: wganLoss,
                        borderColor: '#8b5cf6', // Secondary Purple
                        backgroundColor: 'rgba(139, 92, 246, 0.1)',
                        borderWidth: 3,
                        tension: 0.4, // Smoother
                        pointRadius: 0
                    }
                ]
            },
            options: {
                ...commonChartOptions,
                plugins: {
                    ...commonChartOptions.plugins,
                    title: {
                        display: true,
                        text: 'Training Stability: Loss Convergence',
                        color: '#f8fafc',
                        font: { size: 16 }
                    }
                },
                scales: {
                    x: { display: true, grid: { display: false } },
                    y: { 
                        title: { display: true, text: 'Discriminator Loss', color: '#94a3b8' },
                        grid: { color: '#334155' },
                        ticks: { color: '#94a3b8' }
                    }
                }
            }
        });

        // --- CHART 2: Plotly 3D Scatter (Embeddings) ---
        // Generating random clusters
        function generateCluster(n, cx, cy, cz, noise) {
            const x = [], y = [], z = [];
            for (let i = 0; i < n; i++) {
                x.push(cx + (Math.random() - 0.5) * noise);
                y.push(cy + (Math.random() - 0.5) * noise);
                z.push(cz + (Math.random() - 0.5) * noise);
            }
            return {x, y, z};
        }

        const cluster1 = generateCluster(50, 5, 5, 5, 3); // Cats
        const cluster2 = generateCluster(50, -5, -5, 5, 3); // Dogs
        const cluster3 = generateCluster(50, 0, 0, -5, 3); // Cars

        const trace1 = {
            x: cluster1.x, y: cluster1.y, z: cluster1.z,
            mode: 'markers',
            type: 'scatter3d', // Plotly 3D
            marker: { size: 4, color: '#06b6d4' }, // Primary Cyan
            name: 'Class A (Positive)'
        };

        const trace2 = {
            x: cluster2.x, y: cluster2.y, z: cluster2.z,
            mode: 'markers',
            type: 'scatter3d',
            marker: { size: 4, color: '#f43f5e' }, // Accent Rose
            name: 'Class B (Negative)'
        };

        const trace3 = {
            x: cluster3.x, y: cluster3.y, z: cluster3.z,
            mode: 'markers',
            type: 'scatter3d',
            marker: { size: 4, color: '#8b5cf6' }, // Secondary Purple
            name: 'Class C (Negative)'
        };

        const layout3d = {
            paper_bgcolor: 'rgba(0,0,0,0)',
            plot_bgcolor: 'rgba(0,0,0,0)',
            showlegend: true,
            legend: { x: 0, y: 1, font: { color: 'white' } },
            margin: { l: 0, r: 0, b: 0, t: 0 },
            scene: {
                xaxis: { title: '', showgrid: true, gridcolor: '#334155', zeroline: false, showticklabels: false },
                yaxis: { title: '', showgrid: true, gridcolor: '#334155', zeroline: false, showticklabels: false },
                zaxis: { title: '', showgrid: true, gridcolor: '#334155', zeroline: false, showticklabels: false },
                bgcolor: 'rgba(0,0,0,0)'
            }
        };

        Plotly.newPlot('plotly3d', [trace1, trace2, trace3], layout3d, {displayModeBar: false});


        // --- CHART 3: Attention (Bubble Chart) ---
        const ctxAttn = document.getElementById('attentionChart').getContext('2d');
        
        // Simulating Attention Scores between words: "The cat sat on the mat"
        // Words: The(0), cat(1), sat(2), on(3), the(4), mat(5)
        // 'sat'(2) should attend strongly to 'cat'(1) and 'on'(3)
        const bubbleData = [
            {x: 2, y: 1, r: 15}, // sat -> cat
            {x: 2, y: 3, r: 10}, // sat -> on
            {x: 5, y: 3, r: 12}, // mat -> on
            {x: 1, y: 0, r: 8},  // cat -> The
            {x: 5, y: 4, r: 8},  // mat -> the
            {x: 0, y: 0, r: 5},  // self
            {x: 1, y: 1, r: 5},  // self
            {x: 2, y: 2, r: 5},  // self
        ];

        new Chart(ctxAttn, {
            type: 'bubble',
            data: {
                labels: processLabels(['The', 'cat', 'sat', 'on', 'the', 'mat']),
                datasets: [{
                    label: 'Attention Weight',
                    data: bubbleData,
                    backgroundColor: '#10b981', // Success Emerald
                    borderColor: '#064e3b',
                }]
            },
            options: {
                ...commonChartOptions,
                plugins: {
                    ...commonChartOptions.plugins,
                    tooltip: {
                        callbacks: {
                            title: (items) => {
                                const words = ['The', 'cat', 'sat', 'on', 'the', 'mat'];
                                const item = items[0];
                                return `${words[item.raw.x]} -> ${words[item.raw.y]}`;
                            },
                            label: (item) => `Weight: ${item.raw.r}`
                        }
                    }
                },
                scales: {
                    x: {
                        type: 'linear',
                        position: 'bottom',
                        min: -1, max: 6,
                        ticks: {
                            callback: function(value) {
                                const words = ['The', 'cat', 'sat', 'on', 'the', 'mat'];
                                return words[value] || '';
                            },
                            color: '#94a3b8'
                        },
                        grid: { display: false }
                    },
                    y: {
                        min: -1, max: 6,
                        ticks: {
                            callback: function(value) {
                                const words = ['The', 'cat', 'sat', 'on', 'the', 'mat'];
                                return words[value] || '';
                            },
                            color: '#94a3b8'
                        },
                        grid: { color: '#334155' }
                    }
                }
            }
        });

        // --- CHART 4: Robustness (Radar Chart) ---
        const ctxRadar = document.getElementById('radarChart').getContext('2d');
        
        new Chart(ctxRadar, {
            type: 'radar',
            data: {
                labels: processLabels(['L-Infinity Attack', 'L2 Attack', 'L0 Attack', 'Common Corruptions', 'Clean Accuracy']),
                datasets: [
                    {
                        label: 'Standard Model',
                        data: [10, 20, 15, 40, 95], // Weak against attacks
                        fill: true,
                        backgroundColor: 'rgba(244, 63, 94, 0.2)', // Red
                        borderColor: '#f43f5e',
                        pointBackgroundColor: '#f43f5e',
                    },
                    {
                        label: 'PGD Robust Model',
                        data: [65, 70, 60, 65, 85], // Stronger against attacks, slight drop in clean
                        fill: true,
                        backgroundColor: 'rgba(6, 182, 212, 0.2)', // Cyan
                        borderColor: '#06b6d4',
                        pointBackgroundColor: '#06b6d4',
                    }
                ]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                elements: { line: { borderWidth: 3 } },
                plugins: {
                    tooltip: commonTooltipOptions,
                    legend: { labels: { color: '#f8fafc' } }
                },
                scales: {
                    r: {
                        angleLines: { color: '#334155' },
                        grid: { color: '#334155' },
                        pointLabels: { color: '#f8fafc', font: { size: 12 } },
                        ticks: { backdropColor: 'transparent', color: '#94a3b8' }
                    }
                }
            }
        });

        // --- CHART 5: Future Trends (Doughnut) ---
        const ctxTrend = document.getElementById('trendChart').getContext('2d');
        
        new Chart(ctxTrend, {
            type: 'doughnut',
            data: {
                labels: processLabels(['Non-Euclidean (Hyperbolic)', 'Semantic/LLM Distance', 'Diffusion/Score Based', 'Classic Euclidean']),
                datasets: [{
                    data: [30, 40, 20, 10],
                    backgroundColor: [
                        '#8b5cf6', // Purple
                        '#10b981', // Emerald
                        '#06b6d4', // Cyan
                        '#64748b'  // Slate
                    ],
                    borderColor: '#0f172a',
                    borderWidth: 2
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                plugins: {
                    legend: { position: 'bottom', labels: { color: '#f8fafc' } },
                    tooltip: commonTooltipOptions
                }
            }
        });
    </script>
</body>
</html>
