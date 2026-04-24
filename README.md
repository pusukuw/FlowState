# FlowState

## Description

FlowState is a productivity application designed to help users enter and maintain a state of deep focus, commonly known as "flow." It achieves this through a combination of focused timers, distraction blocking, and ambient noise generation. The application is designed to be simple to use, customizable, and effective in boosting productivity for various tasks, from coding and writing to studying and creative work.

FlowState aims to combat the common pitfalls of procrastination and distraction that plague modern work environments. By providing a structured environment with clearly defined work intervals and break periods, it helps users develop better focus habits and achieve more in less time.

## Features

*   **Focus Timers:** Customizable work and break timers with optional Pomodoro-style intervals.
*   **Distraction Blocking:** Option to block distracting websites and applications during focus sessions. (Platform-specific implementation details below)
*   **Ambient Noise Generation:** Integrated ambient noise player with a selection of nature sounds, white noise, and other calming audio options. Customizable volume levels.
*   **Session History:** Track your focus sessions, including start and end times, duration, and notes.
*   **Customizable Themes:** Choose from a range of visual themes to personalize the application.
*   **Task Management:** Simple task list to keep track of what needs to be done during your focus sessions.
*   **Statistics and Progress Tracking:** Visualize your progress with daily, weekly, and monthly statistics on focus time.
*   **Notifications:** Customizable notifications to signal the start and end of work and break intervals.
*   **(Future) Integrations:** Planned integrations with popular calendar and task management applications.

## Technologies Used

*   **Frontend:**
    *   React: JavaScript library for building user interfaces
    *   Redux: State management library
    *   Styled-Components: CSS-in-JS styling solution
*   **Backend:**
    *   Node.js: JavaScript runtime environment
    *   Express.js: Web application framework for Node.js
    *   MongoDB: NoSQL database for storing user data and session history
*   **Other:**
    *   Electron (if applicable): Framework for building cross-platform desktop applications with JavaScript, HTML, and CSS. (This depends on whether we're targeting desktop)
    *   [Specific library for ambient noise generation, e.g., Tone.js]: Library used for generating and manipulating audio. (Replace with actual library used)
    *   [Specific library for website/application blocking, if any]: Library used for implementing distraction blocking functionality. (Replace with actual library used and note platform-specific limitations)

## Installation

### Prerequisites

*   Node.js (version >= 16)
*   npm (version >= 8) or yarn (version >= 1)
*   MongoDB (if running the backend locally)

### Steps

1.  **Clone the repository:**

    ```bash
    git clone [repository URL]
    cd FlowState
    ```

2.  **Install dependencies:**

    ```bash
    npm install # or yarn install
    ```

3.  **Configure the backend (if necessary):**

    *   If running MongoDB locally, ensure it is running.
    *   If using a remote MongoDB instance, configure the connection string in the `.env` file. Create a `.env` file in the `backend` directory (if it doesn't exist) and add the following:

        ```
        MONGODB_URI=mongodb://[username:password@]host[:port]/database
        ```

4.  **Start the backend:**

    ```bash
    cd backend
    npm run start # or yarn start
    ```

    (This will typically start the backend server on port 3000)

5.  **Start the frontend:**

    ```bash
    cd frontend
    npm run start # or yarn start
    ```

    (This will typically start the frontend development server on port 3001)

6.  **(If Electron) Build the application:**

    If the application is built with Electron:

    ```bash
    npm run build # or yarn build
    ```

    Refer to the Electron documentation for platform-specific build instructions.

## Usage

1.  Open the application in your browser (typically `http://localhost:3001`).
2.  Create an account or log in.
3.  Configure your desired focus and break intervals.
4.  Select ambient noise (optional).
5.  Enter the websites or applications you want to block during focus sessions (if applicable).
6.  Start a focus session!

## Contributing

We welcome contributions to FlowState! Please see our [CONTRIBUTING.md](CONTRIBUTING.md) file for details on how to contribute. Guidelines include submitting pull requests with clear descriptions, adhering to the project's coding style, and providing unit tests for new features.

## License

This project is licensed under the [MIT License](LICENSE).

## Distraction Blocking Notes (Important)

The implementation of distraction blocking varies depending on the platform and the capabilities of the underlying operating system.

*   **Web Browser (if deployed as a web app):** Limited to blocking websites through browser extensions or APIs. Full application blocking is not possible.
*   **Desktop Application (Electron):** More control over blocking applications, but may require elevated privileges or platform-specific APIs. Requires thorough testing on each target operating system (Windows, macOS, Linux). The specific method used for blocking applications will be documented in the code and may involve modifying system settings or using third-party libraries.
*   **Mobile Application (if applicable):** Similar limitations to web browsers, with device-level application blocking requiring root access or specialized APIs.

**Disclaimer:** Distraction blocking functionality is provided as-is and may not be foolproof. Users are responsible for ensuring that the application is configured correctly and that they understand the limitations of the blocking mechanism. We are not responsible for any unintended consequences of using the distraction blocking feature.

## Future Enhancements

*   Integration with calendar applications (Google Calendar, Outlook Calendar)
*   Integration with task management applications (Todoist, Asana, Trello)
*   Advanced statistics and reporting
*   Customizable ambient noise playlists
*   Mobile application version
*   Improved distraction blocking capabilities

## Support

For bug reports, feature requests, or general inquiries, please open an issue on our [GitHub repository]([repository URL]).