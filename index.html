import React, { useState, useEffect } from 'react';
import { BookOpen, User, ArrowLeft, CheckCircle, Clock, Award, PlayCircle } from 'lucide-react';

// --- Graphura Induction Data (with Google Drive File IDs) ---
// NOTE: These are mock file IDs. Replace 'MOCK_FILE_ID_...' with the actual file IDs 
// from your Google Drive videos. Ensure the videos are set to "Anyone with the link can view."

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
      driveFileId: "MOCK_FILE_ID_101" 
    },
    { 
      id: 102, 
      title: "2. Graphura: Vision, Mission & Journey", 
      content: "Explore our founding principles, understand our core identity in Data Visualization and BI, and review key company milestones that led us here. Our Vision is to be the leading provider of data visualization solutions in India. Watch the video for a compelling presentation on our future goals.",
      driveFileId: "MOCK_FILE_ID_102"
    },
    { 
      id: 103, 
      title: "3. Company Culture & Core Values", 
      content: "A deep dive into our core values: Integrity, Innovation, Client-Centricity, and Collaboration. Understand the open-door policy and the focus on work-life harmony. The video provides real-life examples from current employees on how we live these values.",
      driveFileId: "MOCK_FILE_ID_103"
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

// --- Components ---

/**
 * Google Drive Video Embed Component.
 * It uses the specific Google Drive embed URL format.
 */
const DriveVideoEmbed = ({ driveFileId, lessonTitle }) => {
  // Construct the Google Drive embed URL. 
  // Note: 'preview' is crucial for iframe embedding.
  const embedUrl = `https://drive.google.com/file/d/${driveFileId}/preview`;

  // We are using a fixed '16:9' aspect ratio for video presentation
  return (
    <div className="relative w-full aspect-video rounded-xl overflow-hidden shadow-2xl mb-6 border-4 border-indigo-600">
      <iframe
        className="absolute top-0 left-0 w-full h-full"
        src={embedUrl}
        title={`Video: ${lessonTitle}`}
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
        allowFullScreen
        loading="lazy"
        frameBorder="0"
      ></iframe>
      {/* Placeholder message if a valid file ID isn't used or access is restricted */}
      {driveFileId.startsWith("MOCK_FILE_ID") && (
        <div className="absolute inset-0 bg-black bg-opacity-70 flex items-center justify-center">
          <p className="text-white p-4 text-center text-lg font-bold">
            [MOCK VIDEO PLAYER: Replace '{driveFileId}' with your actual Google Drive File ID and ensure file sharing settings are public.]
          </p>
        </div>
      )}
    </div>
  );
};


/**
 * Course Detail and Lesson View Component.
 */
const CourseDetail = ({ course }) => {
  const [selectedLesson, setSelectedLesson] = useState(course.lessons[0]);
  const [completedLessons, setCompletedLessons] = useState(() => {
    const stored = localStorage.getItem('graphura_induction_completed');
    return stored ? JSON.parse(stored) : {};
  });

  // Use useEffect to update mock storage whenever completedLessons changes
  useEffect(() => {
    localStorage.setItem('graphura_induction_completed', JSON.stringify(completedLessons));
  }, [completedLessons]);

  const isCompleted = completedLessons[selectedLesson.id];
  const totalLessons = course.lessons.length;
  const lessonsDone = Object.keys(completedLessons).length;
  const completionPercentage = Math.round((lessonsDone / totalLessons) * 100);
  const isCourseComplete = lessonsDone === totalLessons;

  const handleMarkComplete = (lessonId) => {
    setCompletedLessons(prev => ({
      ...prev,
      [lessonId]: true
    }));
  };

  return (
    <div className="p-4 sm:p-8 space-y-8 max-w-7xl mx-auto">

      {/* Course Header & Progress */}
      <div className="bg-indigo-700 text-white p-6 rounded-xl shadow-xl flex flex-col sm:flex-row justify-between items-start sm:items-center">
        <div>
          <h1 className="text-3xl sm:text-4xl font-extrabold mb-1">{course.title}</h1>
          <p className="text-indigo-200">{course.description}</p>
          <div className="flex flex-wrap text-sm gap-4 mt-3">
            <span className="flex items-center"><User size={16} className="mr-1" /> {course.instructor}</span>
            <span className="flex items-center"><Clock size={16} className="mr-1" /> {course.duration}</span>
          </div>
        </div>
        
        {/* Progress Bar */}
        <div className="mt-4 sm:mt-0 w-full sm:w-48 bg-indigo-600 rounded-full h-3">
          <div 
            className="bg-green-400 h-3 rounded-full transition-all duration-500" 
            style={{ width: `${completionPercentage}%` }}
            role="progressbar"
            aria-valuenow={completionPercentage}
            aria-valuemin="0"
            aria-valuemax="100"
          ></div>
          <p className="text-xs mt-2 text-center sm:text-right font-medium">{completionPercentage}% Complete ({lessonsDone}/{totalLessons})</p>
        </div>
      </div>

      {isCourseComplete && (
        <div className="bg-green-100 border-l-4 border-green-500 text-green-700 p-4 rounded-lg shadow-md flex items-center justify-center">
          <Award size={24} className="mr-3" />
          <p className="font-bold text-lg">Congratulations! You have completed the Graphura New Hire Induction Course!</p>
        </div>
      )}

      <div className="grid grid-cols-1 lg:grid-cols-3 gap-6">
        
        {/* Lesson Content Area (Main View) */}
        <div className="lg:col-span-2 space-y-6">
          <div className="bg-white p-6 rounded-xl shadow-lg border">
            <h2 className="text-2xl font-bold text-gray-900 mb-4 flex items-center">
              <BookOpen size={24} className="mr-2 text-indigo-500" />
              {selectedLesson.title}
            </h2>
            
            {/* --- GOOGLE DRIVE VIDEO EMBED INTEGRATION --- */}
            {selectedLesson.driveFileId && (
              <DriveVideoEmbed 
                driveFileId={selectedLesson.driveFileId} 
                lessonTitle={selectedLesson.title} 
              />
            )}
            
            {/* Content Display Area */}
            <div className="prose max-w-none text-gray-700 leading-relaxed mb-6">
              <p>{selectedLesson.content}</p>
              
              {/* Example of adding detailed content structure from the agenda */}
              {selectedLesson.id === 102 && (
                <div className="mt-4 border-t pt-4">
                  <h3 className="text-lg font-semibold text-gray-800">Vision & Mission Summary</h3>
                  <ul className="list-disc list-inside ml-4 text-sm">
                    <li>**Vision:** To be the leading provider of data visualization and business intelligence solutions in India.</li>
                    <li>**Mission:** We deliver innovative, high-quality, and user-centric software and consulting services, fostering a culture of continuous learning and customer success.</li>
                  </ul>
                </div>
              )}

              {selectedLesson.id === 104 && (
                <div className="mt-4 border-t pt-4">
                  <h3 className="text-lg font-semibold text-gray-800">Key Policies Highlight</h3>
                  <p className="text-sm">Please refer to the HRIS portal for full documentation.</p>
                  <ul className="list-disc list-inside ml-4 text-sm">
                    <li>**Leave:** [X] Casual, [Y] Sick, [Z] Annual days per year.</li>
                    <li>**Confidentiality:** Strict adherence required for client and internal data protection.</li>
                    <li>**Payroll:** Credited on the [Date] of every month.</li>
                  </ul>
                </div>
              )}
            </div>
            
            {/* Completion Button */}
            <div className="pt-4 border-t mt-6">
              <button
                onClick={() => handleMarkComplete(selectedLesson.id)}
                disabled={isCompleted}
                className={`w-full py-3 px-4 rounded-lg text-white font-semibold transition duration-300 flex items-center justify-center ${
                  isCompleted
                    ? 'bg-green-500 cursor-not-allowed'
                    : 'bg-indigo-600 hover:bg-indigo-700 shadow-md'
                }`}
              >
                {isCompleted ? (
                  <>
                    <CheckCircle size={20} className="mr-2" />
                    Completed
                  </>
                ) : (
                  <>
                    <BookOpen size={20} className="mr-2" />
                    Mark Lesson as Complete
                  </>
                )}
              </button>
              
              <p className="text-xs text-gray-500 mt-2 text-center">
                This progress will be saved in your browser (mock storage).
              </p>
            </div>
          </div>
        </div>

        {/* Lesson Navigation (Sidebar) */}
        <div className="lg:col-span-1">
          <div className="bg-white p-4 rounded-xl shadow-lg border">
            <h3 className="text-xl font-semibold mb-4 text-gray-800">Induction Modules</h3>
            <ul className="space-y-2">
              {course.lessons.map(lesson => {
                const isLessonCompleted = completedLessons[lesson.id];
                return (
                  <li
                    key={lesson.id}
                    onClick={() => setSelectedLesson(lesson)}
                    className={`p-3 rounded-lg text-sm transition duration-150 cursor-pointer flex justify-between items-center ${
                      selectedLesson.id === lesson.id
                        ? 'bg-indigo-500 text-white shadow-md'
                        : isLessonCompleted
                          ? 'bg-green-50 text-gray-800 hover:bg-green-100'
                          : 'bg-gray-50 text-gray-800 hover:bg-indigo-100'
                    }`}
                  >
                    <span className={`${selectedLesson.id === lesson.id ? 'font-bold' : ''}`}>
                      {lesson.title}
                    </span>
                    {isLessonCompleted ? (
                      <CheckCircle size={16} className={`${selectedLesson.id === lesson.id ? 'text-white' : 'text-green-500'}`} />
                    ) : (
                      <BookOpen size={16} />
                    )}
                  </li>
                );
              })}
            </ul>
          </div>
        </div>
      </div>
    </div>
  );
};

/**
 * Main Application Component.
 */
const App = () => {
  // Mock user state
  const userName = "New Joiner";

  return (
    <div className="min-h-screen bg-gray-100 font-sans">
      
      {/* Header */}
      <header className="bg-white shadow sticky top-0 z-10">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
          <div className="text-2xl font-extrabold text-indigo-600">
            Graphura Learning Hub
          </div>
          <div className="text-sm font-medium text-gray-700 flex items-center">
            <div className="hidden sm:block mr-3">Induction for <span className="font-bold">{userName}</span></div>
            <div className="w-8 h-8 rounded-full bg-indigo-500 text-white flex items-center justify-center text-xs font-semibold">
              NJ
            </div>
          </div>
        </div>
      </header>

      <main className="pb-12">
        <CourseDetail course={graphuraInductionCourse} />
      </main>
      
      {/* Footer */}
      <footer className="bg-white border-t border-gray-200 text-center py-4 text-sm text-gray-500">
        &copy; {new Date().getFullYear()} Graphura India Private Limited. All Rights Reserved.
      </footer>
    </div>
  );
};

export default App;


