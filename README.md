# Calendar-Applications-For-Communication-Tracking-app

# What is the use of this Repo
This Project is a Simple ReactJS Project which demonstrates the following

# Simple ReactJS Project Template

This project demonstrates the following key features of ReactJS:

- Creating a Component in React
- Making HTTP calls
- Communicating between parent and child components
- Using Bootstrap along with React
- Using Basic Routing in React

This project template can be used as a foundation to build bigger ReactJS projects.

## Prerequisites

### 1. Install Node.js
- Visit [Node.js website](https://nodejs.org/en/) and download the latest stable version of Node.js. Follow the instructions based on your operating system to install Node.js.

### 2. Install `create-react-app`
- Install `create-react-app` globally to easily create and manage React applications. Run the following command in your terminal:

  ```bash
  npm install -g create-react-app 
  
## Live Application URL

After starting the development server using `npm start`, your live application will be accessible at:

- [http://localhost:3000](http://localhost:3000)


# Creating Your First React App with Vite

Follow the steps below to create your first React app using **Vite**.

## Steps to Create Your First React App

### 1. Create a Folder on Your PC
First, create a new folder where you want to store your project files.

### 2. Open the Folder in Visual Studio Code
After creating the folder, open that folder in **Visual Studio Code**.

### 3. Open Your Terminal Window
In Visual Studio Code, open the terminal window by going to **View > Terminal** or using the shortcut `Ctrl + ``.

### 4. Run the Vite Command
In the terminal, type the following command to create a new project using Vite:

```bash
npm create vite@latest
```

### 5. Press 'Y' to Proceed
When prompted, press y to confirm and proceed with creating the project.

### 6. Type Your Project Name
You will be asked to enter the name for your project. Type your desired project name and press Enter.

### 7. Choose React as the Template
You will be prompted to choose a template. Select react from the options.

### 8. Choose React + JavaScript
Next, you’ll be asked if you want to use React with JavaScript or TypeScript. Choose React + JavaScript.

### 9. Navigate to Your Project Folder
```bash
cd <your-project-name>
```
Replace <your-project-name> with the name you provided earlier.

### 10. Install NPM Packages
Now, install all the required npm packages by running the following command:

```
npm install
```

### 11. Run the Application
Finally, run the application locally using the following command:

```
npm run dev
```
Your application will be running at http://localhost:3000. Open this URL in your browser to see your React app in action.

# Deploying Your React App on Vercel

This guide will help you deploy your React app to Vercel.

## Steps to Deploy

### 1. Create a Vercel Account
- Visit [Vercel](https://vercel.com/) and sign up for a free account if you don't already have one.

### 2. Install Vercel CLI
To deploy using the Vercel CLI, you need to install it globally on your system. Run the following command:

```bash
npm install -g vercel
```
### 3. Log in to Vercel
Log in to your Vercel account by running the following command:

```
vercel login
```
You'll be prompted to enter your email address, and then you’ll receive a confirmation email. Follow the instructions to log in.

### 4. Initialize Your Project with Vercel
Navigate to the root directory of your React project and run the following command:
```
vercel
```
This command will guide you through a setup process. If this is your first time deploying, it will ask for:
Project name
Directory to deploy (press Enter to use the current directory)
Link to an existing project (or create a new one)
### 5. Deploy the Application
Once your project is initialized with Vercel, you can deploy your React app with the following command:

```
vercel --prod
```
This will deploy your app to Vercel and make it live. The --prod flag ensures the deployment goes to the production environment.

### 6. Access Your Deployed App
After the deployment finishes, Vercel will provide a URL where your app is hosted. You can access your live application using the provided URL.

### App.jsx
# React Calendar Application for Communication Tracking

This is a React application designed to help track communications with companies. The app includes several components for managing companies, communications, calendar views, and reporting analytics.

## Features
- **Company Management**: Manage and view companies and their communication history.
- **Communication Method Management**: Manage communication methods used for interactions with companies.
- **Dashboard**: View communication data and track important tasks.
- **Notifications**: Get notified about overdue or upcoming communications.
- **Calendar View**: View scheduled communications in a calendar format.
- **Reporting and Analytics**: Generate and display communication reports and analytics.

## Requirements
- Node.js (version 14.x or higher)
- npm (version 6.x or higher)

## Setup Instructions

### 1. Clone the Repository
Clone the project repository to your local machine using the following command:

```bash
git clone <repository-url>
```
2. Install Dependencies
Navigate to the project directory and install the required npm packages:

```
cd <project-folder>
npm install
```
3. Start the Application
Run the application locally:

```
npm start
```
The application will be available at http://localhost:3000.

### Application Design
### Components
Company Management: Displays and manages a list of companies.
Communication Method Management: Manages communication methods (e.g., LinkedIn, Email, Phone Call).
Dashboard: Provides a visual overview of communications.
Notifications: Sends notifications based on the communication schedule.
Calendar View: Displays communications in a calendar format.
Reporting and Analytics: Displays communication reports and analytics.
State Management
companies: An array containing company details, communication history, and next scheduled communication.
showCommunicationModal: Controls the visibility of the modal for adding new communication.
selectedCompany: Tracks the currently selected company for adding communication.

## Folder Structure
plaintext
```
src/
  components/
    CalendarView.js         // Calendar View Component
    CompanyManagement.js    // Company Management Component
    CommunicationMethodManagement.js // Communication Method Management Component
    Dashboard.js            // Dashboard Component
    Notifications.js        // Notifications Component
    ReportingAnalytics.js  // Reporting and Analytics Component
  App.js                    // Main App Component
  index.js                  // Entry point of the application
```
### Example of the companies state:
javascript
const [companies, setCompanies] = useState([
  {
    name: 'Company A',
    communications: [
      { type: 'LinkedIn Post', date: '2023-09-01', notes: 'Initial contact' },
      { type: 'Email', date: '2023-09-05', notes: 'Follow-up' },
    ],
    nextCommunication: { type: 'Email', date: '2023-09-10' },
    overdue: false,
    dueToday: false,
  },
  {
    name: 'Company B',
    communications: [
      { type: 'Phone Call', date: '2023-09-02', notes: 'Discussed project' },
      { type: 'LinkedIn Message', date: '2023-09-06', notes: 'Sent proposal' },
    ],
    nextCommunication: { type: 'LinkedIn Post', date: '2023-09-08' },
    overdue: true,
    dueToday: false,
  },
]);

### Key Functions
handleCommunicationPerformed: Adds a new communication for the selected company and updates the state.
handleAddCommunication: Adds new communication to a specified company and updates the state.
