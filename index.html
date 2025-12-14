<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Graphura Learning Hub</title>
    <!-- Load Tailwind CSS from CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Configure Tailwind to use the Inter font (or system fallback) */
        body {
            font-family: 'Inter', sans-serif;
        }

        /* Responsive Aspect Ratio Container for Video Embed */
        .aspect-video-wrapper {
            position: relative;
            width: 100%;
            padding-top: 56.25%; /* 16:9 Aspect Ratio */
        }
        .aspect-video-wrapper iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
        }

        /* Custom scrollbar for lesson list (optional but nice touch) */
        .lesson-list-container {
            max-height: 550px; /* Limit height on larger screens */
            overflow-y: auto;
        }
        .lesson-list-container::-webkit-scrollbar {
            width: 8px;
        }
        .lesson-list-container::-webkit-scrollbar-thumb {
            background-color: #9ca3af;
            border-radius: 4px;
        }
        .lesson-list-container::-webkit-scrollbar-track {
            background-color: #f3f4f6;
        }
    </style>
</head>
<body class="bg-gray-100 min-h-screen">

    <!-- Main Content Container -->
    <div id="app" class="font-sans">
        <!-- Content will be injected here by JavaScript -->
    </div>

    <script>
        // --- Icon SVGs (Equivalent to Lucide/React Icons) ---
        const ICON_BOOK = '<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-4 h-4"><path d="M4 19.5v-15A2.5 2.5 0 0 1 6.5 2H20v20H6.5a2.5 2.5 0 0 1 0-5H20"/></svg>';
        const ICON_CHECK = '<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round" class="w-4 h-4"><path d="M20 6 9 17l-5-5"/></svg>';
        const ICON_USER = '<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-4 h-4 mr-1"><path d="M19 21v-2a4 4 0 0 0-4-4H9a4 4 0 0 0-4 4v2"/><circle cx="12" cy="7" r="4"/></svg>';
        const ICON_CLOCK = '<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-4 h-4 mr-1"><circle cx="12" cy="12" r="10"/><polyline points="12 6 12 12 16 14"/></svg>';
        const ICON_AWARD = '<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-6 h-6 mr-3"><path d="m15.4 16.5-4.4-4.4"/><path d="M14 14.2 8 20"/><path d="M21 11.5a8.3 8.3 0 0 0-6-6.4V3h-6v2.1c-1.3.8-2.4 1.9-3.2 3.2"/><path d="M21 11.5A7.5 7.5 0 0 0 12 10a7.5 7.5 0 0 0-9 8.2c.2.6.4 1.2.7 1.8h17.2c.3-.6.5-1.2.7-1.8Z"/></svg>';

        // --- Global State and Data ---
        const USER_NAME = "New Joiner";

        const graphuraInductionCourse = {
            id: 1,
            title: "Graphura India: New Hire Induction Training",
            instructor: "HR & Leadership Team",
            duration: "4 hours",
            description: "Welcome to Graphura! This mandatory training will introduce you to our vision, culture, policies, and the tools you need to succeed.",
            lessons: [
                { 
                    id: 101, 
                    title: "1. Welcome & Introductions", 
                    content: "Formal welcome from the leadership team and quick introductions to your key contacts (HR, Manager, Buddy). The video features the CEO and key department heads personally welcoming you aboard.",
                    driveFileId: "MOCK_FILE_ID_101" // REPLACE WITH ACTUAL FILE ID
                },
                { 
                    id: 102, 
                    title: "2. Graphura: Vision, Mission & Journey", 
                    content: "Explore our founding principles, understand our core identity in Data Visualization and BI, and review key company milestones that led us here. Our Vision is to be the leading provider of data visualization solutions in India. Watch the video for a compelling presentation on our future goals.",
                    driveFileId: "MOCK_FILE_ID_102" // REPLACE WITH ACTUAL FILE ID
                },
                { 
                    id: 103, 
                    title: "3. Company Culture & Core Values", 
                    content: "A deep dive into our core values: Integrity, Innovation, Client-Centricity, and Collaboration. Understand the open-door policy and the focus on work-life harmony. The video provides real-life examples from current employees on how we live these values.",
                    driveFileId: "MOCK_FILE_ID_103" // REPLACE WITH ACTUAL FILE ID
                },
                { 
                    id: 104, 
                    title: "4. HR Essentials, Policies & Benefits", 
                    content: "Detailed review of working hours, leave policies (CL, SL, AL), Code of Conduct, Confidentiality policies, and a summary of your compensation and health benefits."
                },
                { 
                    id: 105, 
                    title: "5. IT Setup & Workplace Guidelines", 
                    content: "Instructions for setting up your access credentials (Email, HRIS), hardware checklist, key software access, and mandatory IT security guidelines (Password Policy, VPN, Device Security)."
                },
                { 
                    id: 106, 
                    title: "6. Next Steps & Resources", 
                    content: "A clear action plan for your first week, including paperwork submission, mandatory training completion, and a list of key contacts (HR, IT, Manager, Buddy)."
                },
            ]
        };

        let selectedLessonId = graphuraInductionCourse.lessons[0].id;
        let completedLessons = {}; // { lessonId: true }

        // --- Utility Functions ---

        /**
         * Loads completion status from browser storage.
         */
        function loadProgress() {
            try {
                const stored = localStorage.getItem('graphura_induction_completed');
                completedLessons = stored ? JSON.parse(stored) : {};
            } catch (e) {
                console.error("Could not load progress from localStorage:", e);
                completedLessons = {};
            }
        }

        /**
         * Saves completion status to browser storage.
         */
        function saveProgress() {
            try {
                localStorage.setItem('graphura_induction_completed', JSON.stringify(completedLessons));
            } catch (e) {
                console.error("Could not save progress to localStorage:", e);
            }
        }

        /**
         * Finds a lesson by its ID.
         */
        function getLessonById(id) {
            return graphuraInductionCourse.lessons.find(lesson => lesson.id === id);
        }

        /**
         * Calculates course completion percentage.
         */
        function getCompletionStatus() {
            const lessonsDone = Object.keys(completedLessons).length;
            const totalLessons = graphuraInductionCourse.lessons.length;
            const percentage = totalLessons > 0 ? Math.round((lessonsDone / totalLessons) * 100) : 0;
            const isComplete = lessonsDone === totalLessons;
            return { lessonsDone, totalLessons, percentage, isComplete };
        }

        /**
         * Handles selecting a new lesson and re-renders the course detail.
         */
        function selectLesson(id) {
            selectedLessonId = id;
            renderCourseDetail();
            window.scrollTo(0, 0); // Scroll to top on lesson change
        }

        /**
         * Marks the current selected lesson as complete, saves, and re-renders.
         */
        function markComplete() {
            if (!completedLessons[selectedLessonId]) {
                completedLessons[selectedLessonId] = true;
                saveProgress();
                renderCourseDetail();
            }
        }


        // --- Rendering Functions ---

        /**
         * Renders the Google Drive Video Embed (iframe).
         */
        function renderVideoEmbed(driveFileId, lessonTitle) {
            const embedUrl = `https://drive.google.com/file/d/${driveFileId}/preview`;
            let content = '';

            if (driveFileId.startsWith("MOCK_FILE_ID")) {
                // Mock placeholder for clarity
                content = `
                    <div class="absolute inset-0 bg-black bg-opacity-70 flex items-center justify-center p-8">
                        <p class="text-white text-center text-lg font-bold">
                            [MOCK VIDEO PLAYER: Replace '${driveFileId}' with your actual Google Drive File ID and ensure file sharing is set to 'Anyone with the link can view.']
                        </p>
                    </div>
                `;
            }

            return `
                <div class="aspect-video-wrapper rounded-xl overflow-hidden shadow-2xl mb-6 border-4 border-indigo-600">
                    <iframe
                        src="${embedUrl}"
                        title="Video: ${lessonTitle}"
                        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                        allowfullscreen
                        loading="lazy"
                        frameborder="0"
                    ></iframe>
                    ${content}
                </div>
            `;
        }

        /**
         * Renders the header of the application.
         */
        function renderHeader() {
            const headerHtml = `
                <header class="bg-white shadow sticky top-0 z-10">
                    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
                        <div class="text-2xl font-extrabold text-indigo-600">
                            Graphura Learning Hub
                        </div>
                        <div class="text-sm font-medium text-gray-700 flex items-center">
                            <div class="hidden sm:block mr-3">Induction for <span class="font-bold">${USER_NAME}</span></div>
                            <div class="w-8 h-8 rounded-full bg-indigo-500 text-white flex items-center justify-center text-xs font-semibold">
                                NJ
                            </div>
                        </div>
                    </div>
                </header>
            `;
            return headerHtml;
        }

        /**
         * Renders the course detail section, including the current lesson and sidebar.
         */
        function renderCourseDetail() {
            const container = document.getElementById('app');
            const lesson = getLessonById(selectedLessonId);
            const status = getCompletionStatus();
            
            if (!lesson) {
                container.innerHTML = 'Lesson not found.';
                return;
            }

            const isCompleted = !!completedLessons[lesson.id];
            
            // 1. Video Player HTML (if available)
            const videoHtml = lesson.driveFileId ? renderVideoEmbed(lesson.driveFileId, lesson.title) : '';
            
            // 2. Completion Button HTML
            const completionButtonClass = isCompleted 
                ? 'bg-green-500 cursor-not-allowed' 
                : 'bg-indigo-600 hover:bg-indigo-700 shadow-md';
            const completionButtonContent = isCompleted
                ? `${ICON_CHECK} Completed`
                : `${ICON_BOOK} Mark Lesson as Complete`;

            // 3. Conditional Detail Content (Mocked from previous markdown)
            let richContent = `<p class="leading-relaxed">${lesson.content}</p>`;

            if (lesson.id === 102) {
                richContent += `
                    <div class="mt-6 pt-4 border-t border-gray-200">
                        <h3 class="text-lg font-semibold text-gray-800 mb-2">Vision & Mission Summary</h3>
                        <ul class="list-disc list-inside ml-4 space-y-1 text-sm text-gray-700">
                            <li><strong>Vision:</strong> To be the leading provider of data visualization and business intelligence solutions in India.</li>
                            <li><strong>Mission:</strong> We deliver innovative, high-quality, and user-centric software and consulting services, fostering a culture of continuous learning and customer success.</li>
                        </ul>
                    </div>
                `;
            } else if (lesson.id === 104) {
                 richContent += `
                    <div class="mt-6 pt-4 border-t border-gray-200">
                        <h3 class="text-lg font-semibold text-gray-800 mb-2">Key Policies Highlight</h3>
                        <p class="text-sm text-gray-500 mb-2">Please refer to the HRIS portal for full documentation.</p>
                        <ul class="list-disc list-inside ml-4 space-y-1 text-sm text-gray-700">
                            <li><strong>Leave:</strong> [X] Casual, [Y] Sick, [Z] Annual days per year.</li>
                            <li><strong>Confidentiality:</strong> Strict adherence required for client and internal data protection.</li>
                            <li><strong>Payroll:</strong> Credited on the [Date] of every month.</li>
                        </ul>
                    </div>
                `;
            }


            // 4. Main Template
            const detailHtml = `
                <main class="max-w-7xl mx-auto py-8">
                    <div class="p-4 sm:p-8 space-y-8">
                        
                        <!-- Course Header & Progress -->
                        <div class="bg-indigo-700 text-white p-6 rounded-xl shadow-xl flex flex-col sm:flex-row justify-between items-start sm:items-center">
                            <div>
                                <h1 class="text-3xl sm:text-4xl font-extrabold mb-1">${graphuraInductionCourse.title}</h1>
                                <p class="text-indigo-200">${graphuraInductionCourse.description}</p>
                                <div class="flex flex-wrap text-sm gap-4 mt-3">
                                    <span class="flex items-center">${ICON_USER} ${graphuraInductionCourse.instructor}</span>
                                    <span class="flex items-center">${ICON_CLOCK} ${graphuraInductionCourse.duration}</span>
                                </div>
                            </div>
                            
                            <!-- Progress Bar -->
                            <div class="mt-4 sm:mt-0 w-full sm:w-48 bg-indigo-600 rounded-full h-3">
                                <div 
                                    class="bg-green-400 h-3 rounded-full transition-all duration-500" 
                                    style="width: ${status.percentage}%"
                                ></div>
                                <p class="text-xs mt-2 text-center sm:text-right font-medium">${status.percentage}% Complete (${status.lessonsDone}/${status.totalLessons})</p>
                            </div>
                        </div>

                        <!-- Completion Banner -->
                        ${status.isComplete ? `
                            <div class="bg-green-100 border-l-4 border-green-500 text-green-700 p-4 rounded-lg shadow-md flex items-center justify-center">
                                ${ICON_AWARD}
                                <p class="font-bold text-lg">Congratulations! You have completed the Graphura New Hire Induction Course!</p>
                            </div>
                        ` : ''}

                        <div class="grid grid-cols-1 lg:grid-cols-3 gap-6">
                            
                            <!-- Lesson Content Area (Main View) -->
                            <div class="lg:col-span-2 space-y-6">
                                <div class="bg-white p-6 rounded-xl shadow-lg border">
                                    <h2 class="text-2xl font-bold text-gray-900 mb-4 flex items-center">
                                        ${ICON_BOOK.replace('w-4 h-4', 'w-6 h-6 mr-2 text-indigo-500')}
                                        ${lesson.title}
                                    </h2>
                                    
                                    ${videoHtml}
                                    
                                    <!-- Content Display Area -->
                                    <div class="text-gray-700 text-base mb-6">
                                        ${richContent}
                                    </div>
                                    
                                    <!-- Completion Button -->
                                    <div class="pt-4 border-t mt-6">
                                        <button id="mark-complete-btn"
                                            onclick="markComplete()"
                                            ${isCompleted ? 'disabled' : ''}
                                            class="w-full py-3 px-4 rounded-lg text-white font-semibold transition duration-300 flex items-center justify-center ${completionButtonClass}"
                                        >
                                            ${completionButtonContent}
                                        </button>
                                        
                                        <p class="text-xs text-gray-500 mt-2 text-center">
                                            This progress is saved locally in your browser.
                                        </p>
                                    </div>
                                </div>
                            </div>

                            <!-- Lesson Navigation (Sidebar) -->
                            <div class="lg:col-span-1">
                                <div class="bg-white p-4 rounded-xl shadow-lg border">
                                    <h3 class="text-xl font-semibold mb-4 text-gray-800">Induction Modules</h3>
                                    <ul class="space-y-2 lesson-list-container">
                                        ${graphuraInductionCourse.lessons.map(l => {
                                            const isLessonCompleted = !!completedLessons[l.id];
                                            const isActive = l.id === selectedLessonId;
                                            const activeClass = isActive 
                                                ? 'bg-indigo-500 text-white shadow-md' 
                                                : isLessonCompleted
                                                    ? 'bg-green-50 text-gray-800 hover:bg-green-100'
                                                    : 'bg-gray-50 text-gray-800 hover:bg-indigo-100';
                                            const icon = isLessonCompleted 
                                                ? ICON_CHECK.replace('w-4 h-4', isActive ? 'text-white' : 'text-green-500')
                                                : ICON_BOOK;

                                            return `
                                                <li
                                                    onclick="selectLesson(${l.id})"
                                                    class="p-3 rounded-lg text-sm transition duration-150 cursor-pointer flex justify-between items-center ${activeClass}"
                                                >
                                                    <span class="${isActive ? 'font-bold' : ''}">
                                                        ${l.title}
                                                    </span>
                                                    ${icon}
                                                </li>
                                            `;
                                        }).join('')}
                                    </ul>
                                </div>
                            </div>
                        </div>
                    </div>
                </main>
                <footer class="bg-white border-t border-gray-200 text-center py-4 text-sm text-gray-500">
                    &copy; ${new Date().getFullYear()} Graphura India Private Limited. All Rights Reserved.
                </footer>
            `;
            
            container.innerHTML = detailHtml;
        }

        /**
         * Main initialization function
         */
        function init() {
            loadProgress();
            const app = document.getElementById('app');
            
            // Render the full structure (Header is sticky, so render separately)
            app.innerHTML = renderHeader();
            
            // Render the main course detail content
            renderCourseDetail();
        }

        // Initialize the application when the window loads
        window.onload = init;
    </script>
</body>
</html>

