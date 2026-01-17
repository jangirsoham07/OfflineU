https://github.com/jangirsoham07/OfflineU/releases

[![OfflineU Releases](https://img.shields.io/badge/OfflineU-Releases-blue?logo=github&logoColor=white)](https://github.com/jangirsoham07/OfflineU/releases)

# OfflineU: Self-Hosted Local Course Loader and Progress Tracker for Learners

<img alt="OfflineU Logo" src="https://img.icons8.com/fluency/96/000000/education.png" height="48" width="48" /> A practical, self-hosted solution to load local courses and track learning progress in a private environment. This project focuses on offline-first learning, enabling you to curate a personal course library, progress metrics, and study plans without relying on external clouds.

- Platform: Desktop (Windows, macOS, Linux)
- Core idea: Keep courses and progress on your device
- Goal: Make local learning simple, reliable, and private

If you want to grab the latest official release build, visit the official Releases page here: https://github.com/jangirsoham07/OfflineU/releases. The page lists the prebuilt installers and assets for different operating systems. For convenience, you can also click the colorful button above to open the same page.

Table of contents
- About OfflineU
- Why choose OfflineU
- Key features
- How OfflineU works
- System architecture
- Getting started
- Installation and setup
- Running from source
- Local data and privacy
- Course library management
- Progress tracking and study plans
- User interface overview
- Data model and storage
- Configuration and customization
- CLI and automation
- Plugins and extensions
- Internationalization and accessibility
- Testing and quality
- Release cycle and maintenance
- Roadmap
- Contributing
- Troubleshooting
- Community and support
- Licensing and attribution
- Acknowledgments

About OfflineU
OfflineU is designed for learners who want a durable, private, offline-capable learning environment. It lets you import courses from downloaded sources, view content offline, and record your progress. It is built to run on your own machine, so you control the data and the learning experience. This repository provides the code, the setup instructions, and the guidance you need to run and extend the system in a local setting.

Why choose OfflineU
- Privacy by design: Your course data stays on your device unless you choose to export.
- Offline-first: You can download content once and study without internet access.
- Self-hosted: No dependency on a third-party service for core features.
- Lightweight and fast: Optimized for quick startup and local retrieval of course content.
- Extensible: A plugin system enables new features without changing core code.
- Cross-platform: Works on Windows, macOS, and Linux with prebuilt installers.

Key features
- Local course library: A well-structured catalog of downloaded courses with modules and lessons.
- Progress tracking: Learn where you left off, visualize progress, and resume later.
- Study planning: Create custom study sessions and schedules.
- Offline content rendering: View text, videos, slides, and supplemental materials without an internet connection.
- Content import: Bring in new courses from downloaded sources or user-provided packs.
- Data portability: Export your course data to share or back up.
- Private data store: All data remains on the host machine unless you opt in to sync.
- Simple UX: A clean, distraction-free interface designed for focused learning.
- Local search: Fast search across courses, modules, and lessons.
- Keyboard friendly: Efficient navigation and quick actions with keyboard shortcuts.
- Accessibility: Clear typography and color contrast for easier reading.
- Localization: Support for multiple languages in the UI.

How OfflineU works
- The app runs as a local desktop application. It uses a lightweight embedded database to store your course catalog, lesson progress, and user preferences.
- Courses come from downloaded content packages. Each package contains metadata, modules, and media assets necessary to render content offline.
- The UI presents a browsable library, a reader for course content, and a progress dashboard.
- You choose to keep data on the device by default. If you enable optional sync, you can selectively export progress or import data to a private server you control.
- The system is designed to handle large catalogs without bogging down the host machine. It employs lazy loading and caching to ensure a snappy experience.

System architecture
- Desktop frontend: A cross-platform UI built for speed and clarity.
- Local data store: A lightweight database for catalog, progress, and settings.
- Content renderer: A module capable of rendering text, slides, and video content offline.
- Import pipeline: A mechanism to ingest content from downloaded sources and organize it into a coherent library.
- Plugin interface: A defined boundary for extensions without impacting core functionality.
- Optional sync layer: A privacy-preserving export/import path for progress data.

Getting started
- Prerequisites: A supported desktop operating system (Windows, macOS, Linux). The Releases page contains prebuilt installers you can run directly.
- Access the official Releases page to download installers for your OS. For convenience, you can click the badge near the top of this document to navigate to the same page.
- After installation, launch OfflineU and follow the on-screen prompts to set up your local course library.

Installation and setup
- Quick start with official releases
  - Windows: Run the Windows installer from the Releases page. The installer guides you through the setup. You get a desktop icon and a self-contained data space on your machine.
  - macOS: Open the macOS package (DMG or PKG) from the Releases page. Drag the app to Applications and launch it.
  - Linux: Use the AppImage or distribution-specific package provided in Releases. Make the binary executable and run it.
- From source (optional)
  - Install prerequisites: Node.js 18+ (or the minimum required by the project), a package manager (npm or Yarn), and a local runtime (Electron runtime if applicable).
  - Clone the repository: git clone https://github.com/jangirsoham07/OfflineU.git
  - Install dependencies: npm install
  - Build and run: npm run build && npm start
  - Running from source gives you full control to modify the UI, content rendering, and import logic.
- First run
  - When you start OfflineU for the first time, you will be guided through creating a local library folder. You can point to content packs you have downloaded.
  - The app discovers content in your local library and builds a catalog with a search index. It then loads the initial dashboard to show your current progress and available courses.
- Verifying the release
  - Always use the official releases for install. If the link is not accessible, check the Releases section for alternate mirrors or archives. The Releases page is the authoritative source for installers and validation files.

Releases and downloads
- Access the official releases at: https://github.com/jangirsoham07/OfflineU/releases
- What you will find there
  - Prebuilt installers for Windows, macOS, and Linux
  - AppImages or platform-specific packaging
  - Content packs and sample packages to seed your library
  - Release notes and changelog
- How to use the assets
  - Pick the asset that matches your OS and architecture.
  - Download the file and run it. If you see a security prompt, confirm that you trust the source and that you are running a file from a verified release.
  - After installation, import your content and start tracking progress.
- If the link has a path part (as in the Releases page), the file to download is the installer or asset for your platform. The path indicates a resource you can fetch and run. The installation process will guide you to configure the local library, then you can begin your offline learning journey.
- If the link is not working, or you want to explore before installing, visit the Releases section on the project page to locate the latest stable assets and notes.

Long-form overview of the user journey
- Discover a course
  - Use the library browser to locate courses by title, author, language, or topic. The search index is optimized for quick results even when your catalog grows large.
  - Filter by tag, rating, or date added.
- Import content
  - Import content from downloaded packages. Each package is structured to contain metadata, modules, and assets. The system validates the package, imports it into your catalog, and makes it available for reading.
  - When you import content, the app creates a local index and stores module and lesson data in a way that supports offline rendering.
- Read and learn
  - Open a course to view modules and lessons. The reader supports text, images, slides, and embedded media that you downloaded with the content.
  - You can switch between modules, mark lessons as complete, and set a preferred playback or reading mode.
- Track progress
  - The progress dashboard shows completion percentages, time spent, and upcoming lessons.
  - The system records your activity locally. You can export progress to back up or share with a trusted partner.
- Plan study sessions
  - Create study plans with goals, deadlines, and reminders.
  - Schedule sessions for specific days and times. The app can help you stay on track with gentle nudges and a clear overview of upcoming tasks.
- Export and portability
  - If you ever want to move your data, export your library and progress in a portable format.
  - The export preserves course metadata, module structure, and progress data so you can restore or migrate to another installation.

UI and user experience
- Clean, distraction-free layout
  - A calm color palette and legible typography help reduce cognitive load.
  - The interface is keyboard-friendly. Most actions have consistent shortcuts.
- Library view
  - A catalog of courses with thumbnails, titles, authors, languages, and progress bars.
  - Quick filters and a robust search experience.
- Course reader
  - A content pane that renders textual content, images, slides, and videos from locally stored assets.
  - A side panel shows module structure and a progress indicator.
- Progress dashboard
  - A visual summary of how far you are in each course and your overall learning timeline.
  - The dashboard includes export options and a history of daily activity.
- Settings and preferences
  - Personalize fonts, themes, and reading mode.
  - Configure how content is loaded and cached to balance performance and disk usage.

Data model and storage
- Local SQLite-like store
  - Courses: id, title, author, language, tags, cover image, release date
  - Modules: id, course_id, title, order
  - Lessons: id, module_id, title, content_path, duration, order
  - Progress: lesson_id, completed, timestamp
  - StudyPlans: id, name, due_date, goals
  - Settings: user preferences, display options, privacy controls
- Content packaging
  - Each course package includes a manifest with metadata and a manifest of assets.
  - Assets include text, slides, images, and video files. All assets are stored locally in the library folder.
- Search index
  - A local search index enables fast lookup across titles, tags, and content descriptions.
  - The index is updated whenever new content is imported.

Configuration and customization
- Global settings
  - storagePath: Path to the local library and data store
  - language: UI language
  - theme: Light or dark
  - autoplayMedia: Auto-play behavior for multimedia
  - offlineMode: Force offline functionality for sensitive environments
- Content handling
  - contentCacheSize: Limit for local caching to manage disk usage
  - prefetchContent: Prefetch upcoming lessons to reduce latency
  - mediaQuality: Control quality of media files loaded for offline viewing
- Privacy and export
  - syncEnabled: Enable or disable export/import to a private server
  - exportFormat: Choose JSON or a compact binary for data portability
  - encryption: Optional encryption for local exports
- Extensibility
  - pluginPath: Directory for third-party plugins
  - pluginAPI: Public API surface for plugin interaction
  - localizationFiles: Path to translation files for multilingual support

CLI and automation
- The command line interface (CLI) enables automation and integration with local tooling.
- Typical commands (illustrative)
  - offlineu list: Show all courses in the local library
  - offlineu import <path>: Import a course package from a local path
  - offlineu start: Launch the UI in development or production mode
  - offlineu export --format json: Export library data to JSON
  - offlineu progress: Show progress statistics
  - offlineu sync --pull: Pull updates from a configured private server
- Automation workflows
  - Script onboarding: A script that installs dependencies, configures default settings, and seeds the library with initial content
  - Tiered backups: A script that exports progress and library metadata on a scheduled basis
  - Content refresh: A script that checks for updated content packages and imports them automatically

Plugins and extensions
- Plugin system
  - A clearly defined plugin interface allows developers to add features without modifying core code.
  - Examples of plugin capabilities:
    - Alternate readers for different media formats
    - Custom progress visualization widgets
    - External data import from local directories
- Developing plugins
  - Create a plugin manifest with name, version, and entry point
  - Implement hooks for lifecycle events (onImport, onProgressUpdate, onStudySessionStart)
  - Register the plugin with the host app using the pluginPath
- Distribution
  - Plugins can be published to a central store or shared via local file systems
  - Plugins must adhere to the host’s security model and API contracts

Localization and accessibility
- Multilingual UI
  - The app includes language packs for several major languages and supports contribution of new translations.
  - UI strings are designed to be concise and clear to minimize reading complexity.
- Accessibility
  - High contrast themes, scalable font sizes, and keyboard navigation support
  - Screen reader compatibility for essential UI components
  - Clear focus indicators and descriptive labels for actions

Screenshots and visual references
- Library view
  - ![Library view](https://img.icons8.com/fluency/96/000000/library.png)
- Course reader
  - ![Course reader](https://img.icons8.com/fluency/96/000000/book.png)
- Progress dashboard
  - ![Progress dashboard](https://img.icons8.com/fluency/96/000000/chart.png)
- Settings
  - ![Settings](https://img.icons8.com/fluency/96/000000/settings.png)

Testing and quality
- Unit tests
  - Focus on core data models, import logic, and progress calculations
- Integration tests
  - Validate the end-to-end flow from importing a course package to updating progress
- UI tests
  - Verify keyboard navigation, focus management, and responsive layout
- Performance checks
  - Ensure fast catalog search and quick rendering of content
- CI/CD
  - Automated tests run on pushes to main and on release branches
  - Artifacts produced for each release with checksums and integrity validation

Release cycle and maintenance
- Release cadence
  - Regular minor releases for bug fixes and small improvements
  - Major releases for new features and architectural changes
- Changelog format
  - Entries include version, date, and a concise summary of changes
  - User-impact notes highlight any breaking changes or migration steps
- Migration notes
  - When upgrading across major versions, follow the documented migration steps
  - Back up local data before applying upgrades to avoid data loss

Roadmap
- Short-term goals
  - Improve import performance for large course catalogs
  - Expand the set of built-in content packs
  - Enhance search capabilities with semantic queries
- Mid-term goals
  - Add socio-cultural localization packs
  - Introduce advanced study planning with calendar integration
  - Implement a richer media player for embedded video and slides
- Long-term goals
  - Build a collaborative study mode with opt-in local sharing
  - Support for offline notes and personal annotations
  - Cross-device synchronization across a trusted private server (optional)

Contributing
- How to contribute
  - Start by opening an issue to discuss enhancements, bug reports, or questions
  - Fork the repository, create a feature branch, and open a pull request
  - Include tests and documentation with new features
- Coding guidelines
  - Follow the project’s style guide for JavaScript/TypeScript, or the language used in the frontend
  - Write unit tests for new features and regression tests for bug fixes
  - Keep changes small and focused to ease reviews
- Example of a contribution flow
  - Create a branch: git checkout -b feature/new-reader
  - Implement changes and tests
  - Run tests locally
  - Submit a pull request with a clear description of the change
- Community etiquette
  - Be respectful and patient in discussions
  - Provide actionable feedback and avoid personal critiques
  - Reference issues and PRs where relevant to maintain context

Troubleshooting
- Common issues
  - Installer fails to run: Ensure the file is from the official Releases page and that your OS matches the installer
  - Content not appearing after import: Confirm the content package contains valid metadata and assets
  - Progress not saving: Check the local data store for write permissions and sufficient disk space
  - UI not rendering correctly: Try a fresh install from the official release; confirm you meet minimum system requirements
- How to gather logs
  - Enable verbose logging in settings to capture startup messages
  - Locate log files in the local data directory to attach in issues
- Getting help
  - Open an issue with a clear description, environment details, and steps to reproduce
  - Share relevant log excerpts to help triage

Releases and validation
- The Releases page is the primary source for installers and assets
- Validate downloaded files using checksums when provided
- If you encounter issues with a release, check the release notes for fixes or downgrades
- The repository encourages users to verify authenticity and integrity of assets from the official page

Security and privacy notes
- Local-first design keeps content and progress on your device by default
- When enabled, sync and export options are designed to be opt-in and controllable
- Data exports can be encrypted to protect sensitive information
- Access to content and progress is governed by local permissions and user settings

License
- OfflineU is distributed under the MIT license
- The license allows wide use, modification, and distribution
- The project disclaims warranties and seeks to provide a transparent, honest experience for learners

Acknowledgments
- Thanks to early adopters and testers who provided feedback
- Appreciation for open-source contributors who added features and fixed bugs
- Gratitude to the community for sharing content and ideas to improve offline learning

Appendix: sample content pack structure
- package.json (metadata)
- manifest.json (describes modules, lessons, assets)
- modules/
  - module-01/
    - title.txt
    - lessons/
      - lesson-01.txt
      - lesson-02.txt
- assets/
  - images/
  - videos/
  - slides/
- index.html or equivalent entry point for rendering

Appendix: sample manifest snippet
- {
  "courseId": "course-101",
  "title": "Foundations of Offline Learning",
  "author": "OfflineU Team",
  "language": "en",
  "modules": [
    {
      "moduleId": "mod-01",
      "title": "Getting Started",
      "lessons": [
        {"lessonId": "les-01", "title": "Welcome", "contentPath": "modules/mod-01/lessons/lesson-01.txt", "duration": 600},
        {"lessonId": "les-02", "title": "Navigation", "contentPath": "modules/mod-01/lessons/lesson-02.txt", "duration": 420}
      ]
    }
  ],
  "assets": ["assets/images/welcome.png", "assets/videos/intro.mp4"]
}

Appendix: example user journey narrative
- You download a course package from a downloaded source and import it into OfflineU.
- The content is parsed, indexed, and added to your library.
- You open the course from the library, read the content, and complete lessons.
- The progress is saved locally, and you can review your daily activity in the dashboard.
- You plan a study session, set a target, and achieve the daily goals.

Appendix: glossary
- Offline-first: A design principle that prioritizes functioning without a network
- Package: A self-contained content bundle with metadata, assets, and structure
- Progress: A record of what you have completed and what remains
- Sync: A feature to push or pull data to a remote server you control
- Plugin: An add-on that extends functionality without touching core code

Releases and checks
- For the most reliable experience, prefer official releases
- The Releases page contains a curated set of assets for your OS
- If you encounter a broken asset or a missing file, report it or check the Releases section for updates

End notes
- OfflineU is designed with practical learning in mind
- It focuses on a private, offline-ready workflow
- The system is built to be approachable for both beginners and power users
- The documentation aims to be thorough, welcoming, and precise

Note: The end of this README avoids a formal conclusion by presenting a comprehensive, structured guide that can stand alone. It is designed to help users understand the project, set up a local environment, and explore ways to customize and extend OfflineU.