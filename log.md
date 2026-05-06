<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Saniya Malik | AI Architect</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link
        href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700&family=Instrument+Serif:italic@400&display=swap"
        rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    <style>
        :root {
            --bg: #0a0a0a;
            --accent: #ffffff;
            --secondary: #71717a;
            --card-bg: #141414;
        }

        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background-color: var(--bg);
            color: var(--accent);
            overflow-x: hidden;
        }

        .serif {
            font-family: 'Instrument Serif', serif;
        }

        /* Case Study Cards */
        .case-study-card {
            position: relative;
            border-radius: 24px;
            overflow: hidden;
            background: var(--card-bg);
            transition: all 0.6s cubic-bezier(0.23, 1, 0.32, 1);
            cursor: pointer;
            border: 1px solid rgba(255, 255, 255, 0.05);
        }

        .case-study-card:hover {
            transform: translateY(-10px);
            border-color: rgba(255, 255, 255, 0.2);
        }

        .case-study-image {
            transition: transform 0.8s ease;
            filter: grayscale(100%);
        }

        .case-study-card:hover .case-study-image {
            transform: scale(1.05);
            filter: grayscale(0%);
        }

        /* Sovereign Section Styling */
        .sovereign-section {
            background: radial-gradient(circle at center, #1a1a1a 0%, #000 100%);
            border: 1px solid #333;
        }

        .pulse-border {
            box-shadow: 0 0 0 0 rgba(255, 255, 255, 0.4);
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% {
                box-shadow: 0 0 0 0 rgba(255, 255, 255, 0.4);
            }

            70% {
                box-shadow: 0 0 0 20px rgba(255, 255, 255, 0);
            }

            100% {
                box-shadow: 0 0 0 0 rgba(255, 255, 255, 0);
            }
        }

        .nav-blur {
            backdrop-filter: blur(15px);
            background: rgba(10, 10, 10, 0.95);
        }

        .text-reveal {
            background: linear-gradient(to right, #fff 20%, #444 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        /* Detail Modal Animation */
        .detail-modal {
            animation: modalFadeIn 0.5s cubic-bezier(0.16, 1, 0.3, 1);
        }

        @keyframes modalFadeIn {
            from {
                opacity: 0;
                transform: translateY(50px);
            }

            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .tech-pill {
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.1);
            padding: 4px 12px;
            border-radius: 100px;
            font-size: 12px;
        }
    </style>
</head>

<body>

    <!-- Navbar -->
    <nav class="fixed top-0 w-full z-50 nav-blur border-b border-white/5">
        <div class="max-w-7xl mx-auto px-8 py-5 flex justify-between items-center">
            <a href="#" class="text-xl font-bold tracking-tighter">SM <span class="text-zinc-500 font-normal">/
                    ARCHITECT</span></a>

            <div class="hidden md:flex gap-12 text-[13px] font-medium tracking-widest uppercase opacity-70">
                <a href="#work" class="hover:opacity-100 transition nav-link">Work</a>
                <a href="#sovereign" class="hover:opacity-100 transition nav-link">Sovereign AI</a>
                <a href="#about" class="hover:opacity-100 transition nav-link">About</a>
                <a href="#contact" class="hover:opacity-100 transition nav-link">Contact</a>
            </div>

            <button onclick="openTalkModal()"
                class="text-sm bg-white text-black px-6 py-2.5 rounded-full font-medium hover:bg-zinc-200 transition">
                Let's Talk
            </button>
        </div>
    </nav>

    <!-- Hero -->
    <section class="min-h-screen flex flex-col justify-center px-8 relative pt-20">
        <div class="max-w-7xl mx-auto w-full">
            <span class="text-zinc-500 font-medium tracking-[0.3em] uppercase text-xs mb-8 block"
                data-aos="fade-up">Generative AI Consultant</span>
            <h1 class="text-6xl md:text-[120px] leading-[0.9] font-bold tracking-tighter mb-12 text-reveal"
                data-aos="fade-up" data-aos-delay="100">
                Building <span class="serif italic font-normal">Intelligence</span><br>That Scales.
            </h1>
            <div class="flex flex-col md:flex-row md:items-end justify-between gap-8">
                <p class="max-w-md text-lg text-zinc-400 leading-relaxed" data-aos="fade-up" data-aos-delay="200">
                    Specializing in production-grade RAG architectures, multi-agent systems, and sovereign AI for
                    high-stakes enterprise environments.
                </p>
                <div class="flex gap-4" data-aos="fade-up" data-aos-delay="300">
                    <div class="flex -space-x-3">
                        <img src="https://i.pravatar.cc/100?u=1"
                            class="w-12 h-12 rounded-full border-4 border-[#0a0a0a]">
                        <img src="https://i.pravatar.cc/100?u=2"
                            class="w-12 h-12 rounded-full border-4 border-[#0a0a0a]">
                        <img src="https://i.pravatar.cc/100?u=3"
                            class="w-12 h-12 rounded-full border-4 border-[#0a0a0a]">
                    </div>
                    <div class="text-sm">
                        <p class="font-bold">12+ Global Partners</p>
                        <p class="text-zinc-500 italic">5-Star Consulting Performance</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Work Section (Case Studies) -->
    <section id="work" class="py-32 px-8">
        <div class="max-w-7xl mx-auto">
            <div class="flex justify-between items-end mb-20">
                <h2 class="text-4xl font-bold tracking-tighter">Selected <span class="serif italic font-normal">Case
                        Studies</span></h2>
                <div class="text-zinc-500 text-sm hidden md:block">01 — 03</div>
            </div>

            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Case Study 1: ClaimLens -->
                <div class="case-study-card group" onclick="openCaseStudy('claimlens')" data-aos="fade-up">
                    <div class="aspect-[4/5] overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1563986768609-322da13575f3?auto=format&fit=crop&q=80&w=800"
                            class="case-study-image w-full h-full object-cover">
                    </div>
                    <div class="p-8">
                        <h3 class="text-2xl font-bold mb-2">ClaimLens AI</h3>
                        <p class="text-zinc-500 text-sm mb-4 uppercase tracking-widest">Fraud Detection System</p>
                        <div
                            class="flex items-center text-sm font-bold border-b border-white w-fit pb-1 group-hover:gap-4 transition-all">
                            View Deep Dive <i class="fa-solid fa-arrow-right-long ml-2"></i>
                        </div>
                    </div>
                </div>

                <!-- Case Study 2: NyaySetu -->
                <div class="case-study-card group" onclick="openCaseStudy('nyaysetu')" data-aos="fade-up"
                    data-aos-delay="100">
                    <div class="aspect-[4/5] overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1589829545856-d10d557cf95f?auto=format&fit=crop&q=80&w=800"
                            class="case-study-image w-full h-full object-cover">
                    </div>
                    <div class="p-8">
                        <h3 class="text-2xl font-bold mb-2">NyaySetu</h3>
                        <p class="text-zinc-500 text-sm mb-4 uppercase tracking-widest">Legal RAG Platform</p>
                        <div
                            class="flex items-center text-sm font-bold border-b border-white w-fit pb-1 group-hover:gap-4 transition-all">
                            View Deep Dive <i class="fa-solid fa-arrow-right-long ml-2"></i>
                        </div>
                    </div>
                </div>

                <!-- Case Study 3: GovGig -->
                <div class="case-study-card group" onclick="openCaseStudy('govgig')" data-aos="fade-up"
                    data-aos-delay="200">
                    <div class="aspect-[4/5] overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1639322537228-f710d846310a?auto=format&fit=crop&q=80&w=1200"
                            class="case-study-image w-full h-full object-cover">
                    </div>
                    <div class="p-8">
                        <h3 class="text-2xl font-bold mb-2">GovGig AI</h3>
                        <p class="text-zinc-500 text-sm mb-4 uppercase tracking-widest">Regulatory Compliance</p>
                        <div
                            class="flex items-center text-sm font-bold border-b border-white w-fit pb-1 group-hover:gap-4 transition-all">
                            View Deep Dive <i class="fa-solid fa-arrow-right-long ml-2"></i>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Sovereign AI (Marketing Flagship) -->
    <section id="sovereign" class="py-32 px-8 overflow-hidden">
        <div class="max-w-7xl mx-auto sovereign-section rounded-[40px] p-12 md:p-24 relative">
            <div class="grid md:grid-cols-2 gap-16 items-center">
                <div data-aos="fade-right">
                    <div class="flex items-center gap-4 mb-8">
                        <span class="w-12 h-[1px] bg-white"></span>
                        <span class="text-xs uppercase tracking-widest font-bold">Flagship Solution</span>
                    </div>
                    <h2 class="text-5xl md:text-7xl font-bold tracking-tighter mb-8 leading-tight">
                        Sovereign <br><span class="serif italic font-normal">Guard.</span>
                    </h2>
                    <p class="text-zinc-400 text-lg mb-10 leading-relaxed">
                        A production-grade LLM safety and observability tower. We don't just build AI; we build
                        <strong>Sovereign</strong> AI that is hallucination-resistant, secure, and entirely under your
                        control.
                    </p>
                    <div class="space-y-6 mb-12">
                        <div class="flex items-center gap-4">
                            <div class="w-2 h-2 rounded-full bg-green-500 pulse-border"></div>
                            <span class="text-sm font-medium">99.8% Groundedness Accuracy</span>
                        </div>
                        <div class="flex items-center gap-4">
                            <div class="w-2 h-2 rounded-full bg-blue-500"></div>
                            <span class="text-sm font-medium">Sub-150ms Deterministic Guardrails</span>
                        </div>
                    </div>
                    <button onclick="openTalkModal()"
                        class="bg-white text-black px-10 py-4 rounded-full font-bold hover:bg-zinc-200 transition">
                        Discuss Implementation
                    </button>
                </div>
                <div class="relative" data-aos="fade-left">
                    <div class="bg-zinc-900 border border-white/10 p-4 rounded-3xl shadow-2xl">
                        <img src="https://images.unsplash.com/photo-1550751827-4bd374c3f58b?auto=format&fit=crop&q=80&w=800"
                            class="rounded-2xl grayscale" alt="Sovereign AI Terminal">
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-32 px-8 bg-[#0d0d0d]">
        <div class="max-w-6xl mx-auto">
            <div class="grid md:grid-cols-12 gap-16 items-center">
                <div class="md:col-span-5" data-aos="fade-up">
                    <img src="https://i.pravatar.cc/800?u=saniya" class="w-full rounded-3xl" alt="Saniya Malik">
                </div>
                <div class="md:col-span-7" data-aos="fade-up" data-aos-delay="200">
                    <h2 class="text-5xl font-bold tracking-tighter mb-8">Hi, I'm Saniya Malik</h2>
                    <div class="prose prose-invert text-zinc-400 text-lg leading-relaxed">
                        <p>AI Architect & Engineer with 7+ years building production AI systems. I help enterprises move
                            from prototypes to reliable, scalable, and secure AI platforms.</p>
                        <p>Formerly led AI initiatives at two Series-B startups. Currently focused on <span
                                class="text-white">Agentic Systems</span>, <span class="text-white">RAG
                                Optimization</span>, and <span class="text-white">Sovereign AI infrastructure</span>.
                        </p>
                    </div>
                    <div class="grid grid-cols-3 gap-8 mt-16">
                        <div>
                            <p class="text-4xl font-bold">40+</p>
                            <p class="text-sm text-zinc-500">Projects Delivered</p>
                        </div>
                        <div>
                            <p class="text-4xl font-bold">12</p>
                            <p class="text-sm text-zinc-500">Enterprise Clients</p>
                        </div>
                        <div>
                            <p class="text-4xl font-bold">99.8%</p>
                            <p class="text-sm text-zinc-500">Avg. Accuracy</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Case Study Modal -->
    <div id="caseStudyModal" class="hidden fixed inset-0 z-[100] bg-black/95 backdrop-blur-xl overflow-y-auto">
        <div class="max-w-5xl mx-auto px-8 py-20 relative">
            <button onclick="closeCaseStudy()"
                class="fixed top-8 right-8 text-4xl hover:rotate-90 transition-transform duration-300">×</button>
            <div id="modalContent" class="detail-modal"></div>
        </div>
    </div>

    <!-- Let's Talk Modal -->
    <div id="talkModal"
        class="hidden fixed inset-0 bg-black/80 backdrop-blur-xl z-[200] flex items-center justify-center p-4">
        <div class="bg-zinc-900 w-full max-w-lg rounded-3xl overflow-hidden border border-white/10 p-8">
            <div class="flex justify-between items-center mb-8">
                <h3 class="text-2xl font-bold">Let's Talk</h3>
                <button onclick="closeTalkModal()" class="text-3xl">&times;</button>
            </div>
            <form id="talkForm" onsubmit="handleTalkSubmit(event)" class="space-y-4">
                <input type="text" id="t_name" placeholder="Name" required
                    class="w-full bg-zinc-800 border border-white/10 rounded-xl px-5 py-3">
                <input type="email" id="t_email" placeholder="Email" required
                    class="w-full bg-zinc-800 border border-white/10 rounded-xl px-5 py-3">
                <textarea id="t_message" rows="4" placeholder="Your Project Details" required
                    class="w-full bg-zinc-800 border border-white/10 rounded-xl px-5 py-3"></textarea>
                <button type="submit" class="w-full bg-white text-black py-4 rounded-xl font-bold">Send Inquiry</button>
            </form>
        </div>
    </div>

    <!-- Contact & Footer -->
    <section id="contact" class="py-32 px-8 text-center">
        <h2 class="text-6xl md:text-8xl font-bold tracking-tighter mb-12 text-reveal">Let's build <br><span
                class="serif italic font-normal">the future.</span></h2>
        <a href="mailto:san192227m@gmail.com"
            class="text-2xl font-medium hover:text-zinc-500 transition">san192227m@gmail.com</a>
        <footer class="mt-32 text-[10px] uppercase tracking-[0.4em] opacity-40">© 2026 Saniya Malik — AI Architect
        </footer>
    </section>

    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    <script>
        AOS.init({ duration: 1000, once: true });

        const projects = {
            claimlens: {
                title: "ClaimLens AI",
                subtitle: "AI-Powered Insurance Fraud Detection",
                overview: "ClaimLens is an advanced multi-modal AI platform designed to detect insurance fraud in real-time, reducing fraudulent payouts for Indian insurance giants.",
                challenge: ["Sophisticated document forgery", "Complex fraud networks", "Support for Hinglish narratives"],
                solution: ["Multi-Engine Scoring (CatBoost)", "Computer Vision (ResNet50)", "Graph Analytics (Neo4j)"],
                tech: ["Python", "Neo4j", "CatBoost", "FastAPI", "Groq LLM"],
                results: ["<2s Processing Time", "Uncovered hidden fraud rings", "92% Accuracy improvement"]
            },
            nyaysetu: {
                title: "NyaySetu",
                subtitle: "Production Legal RAG System",
                overview: "Tailored for Indian Supreme Court judgments, providing reliable analysis with precedent citations and reduced hallucinations.",
                challenge: ["Fragmented legal context", "High-stakes accuracy requirements", "Domain-specific terminology"],
                solution: ["ReflectionRAG", "LLM Verdict Chunking", "InLegalBERT Embeddings"],
                tech: ["LangGraph", "Qdrant", "InLegalBERT", "AWS ECS", "Terraform"],
                results: ["99.8% Factual Grounding", "25,000+ indexed judgments", "Verified by top legal firms"]
            },
            govgig: {
                title: "GovGig AI",
                subtitle: "Regulatory RAG & Compliance Agent",
                overview: "Automated compliance system that monitors government regulations and ensures enterprise documentation meets all legal standards.",
                challenge: ["Daily regulatory changes", "Manual compliance audits", "Fragmented PDF sources"],
                solution: ["Agentic RAG Pipeline", "Automated Policy Mapping", "Source-verified Citations"],
                tech: ["Llama 3", "Vector DB", "FastAPI", "Async Processing"],
                results: ["80% Compliance Automation", "95% Reduction in audit time", "Zero-miss monitoring"]
            }
        };

        function openCaseStudy(id) {
            const p = projects[id];
            const content = document.getElementById('modalContent');
            content.innerHTML = `
                <div class="mb-12">
                    <h2 class="text-5xl md:text-7xl font-bold tracking-tighter mb-4">${p.title}</h2>
                    <p class="text-2xl text-zinc-400 font-medium serif italic">${p.subtitle}</p>
                </div>
                <div class="grid md:grid-cols-3 gap-12">
                    <div class="md:col-span-2">
                        <h4 class="text-lg font-bold mb-4">The Challenge</h4>
                        <ul class="space-y-4 mb-10 text-zinc-400">
                            ${p.challenge.map(c => `<li class="flex gap-3"><span>—</span> ${c}</li>`).join('')}
                        </ul>
                        <h4 class="text-lg font-bold mb-4">Our Solution</h4>
                        <ul class="space-y-4 text-zinc-400">
                            ${p.solution.map(s => `<li class="flex gap-3"><span class="text-white">✓</span> ${s}</li>`).join('')}
                        </ul>
                    </div>
                    <div class="bg-zinc-900 p-8 rounded-3xl border border-white/5 h-fit">
                        <h4 class="text-xs font-bold uppercase tracking-widest mb-6">Tech Stack</h4>
                        <div class="flex flex-wrap gap-2 mb-10">${p.tech.map(t => `<span class="tech-pill">${t}</span>`).join('')}</div>
                        <h4 class="text-xs font-bold uppercase tracking-widest mb-6">Key Results</h4>
                        <div class="space-y-4 text-sm font-bold">${p.results.map(r => `<p>${r}</p>`).join('')}</div>
                    </div>
                </div>
            `;
            document.getElementById('caseStudyModal').classList.remove('hidden');
            document.body.style.overflow = 'hidden';
        }

        function closeCaseStudy() {
            document.getElementById('caseStudyModal').classList.add('hidden');
            document.body.style.overflow = 'auto';
        }

        function openTalkModal() { document.getElementById('talkModal').classList.remove('hidden'); }
        function closeTalkModal() { document.getElementById('talkModal').classList.add('hidden'); }

        function handleTalkSubmit(e) {
            e.preventDefault();
            alert("Inquiry Sent! Check console for debug.");
            closeTalkModal();
        }

        // Smooth Scroll
        document.querySelectorAll('.nav-link').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) window.scrollTo({ top: target.offsetTop - 80, behavior: 'smooth' });
            });
        });
    </script>
</body>

</html>