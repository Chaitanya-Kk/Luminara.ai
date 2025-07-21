Luminara.ai

Luminara.ai is an AI-powered chat assistant built for Adobe Express. It helps users brainstorm ideas, generate content, and stay creative — all from within the Express editor.
✨ Overview
Luminara.ai is an AI-powered chat assistant integrated directly into Adobe Express. Whether you’re designing a social post, flyer, or presentation, Luminara helps you brainstorm ideas, write content, and overcome creative blocks through natural conversation.

🚀 Features

💬 Chat-based AI assistant inside Adobe Express
⚡ Powered by Google Gemini 1.5 Flash for fast, high-quality responses
✍️ Suggests taglines, content, captions, and layout ideas
🧠 Assists with brainstorming and ideation
🖼️ Lightweight UI that doesn’t interfere with your canvas
✅ Built using Adobe Express Add-ons API


🌟 Inspiration
Designers often hit creative walls. We asked:

“What if you could talk to an AI while designing — without switching tabs or tools?”

That led to Luminara.ai — your creative co-pilot that keeps your flow going.

🛠️ How It Works

Open Adobe Express and load the add-on.
Access Luminara.ai in the sidebar panel.
Start chatting! Ask for layout tips, content help, or ideas.
Copy-paste responses into your project if helpful.


🏗️ How It’s Built
1. Project Setup
Started by scaffolding the project using Adobe’s official add-on template:
npx @adobe/create-ccweb-add-on design-chat-addon --entrypoint panel --template javascript

This command set up a basic Adobe Express add-on structure with a panel entry point, using JavaScript as the base language. The template provided index.html, index.js, styles.css, and a manifest.json in the /dist folder.
2. Customizations & Development

UI Development: Modified index.html and styles.css to create a lightweight, non-intrusive chat interface in the Adobe Express sidebar.
Logic Implementation: Replaced the default JavaScript logic in index.js with TypeScript (index.ts) for better type safety and maintainability. Compiled TypeScript to JavaScript using:npx tsc


AI Integration: Integrated Google Gemini 1.5 Flash for real-time chat functionality, making API calls to:const url = 'https://generativelanguage.googleapis.com/v1beta/models/gemini-1.5-flash:generateContent';


Custom Features: Added logic to handle user prompts for design suggestions, content generation, and brainstorming, tailoring responses to fit Adobe Express workflows.

3. Manifest & Configuration

Updated dist/manifest.json to include specific permissions for network access (for Gemini API) and panel configurations for Adobe Express.
Configured entry points and ensured compatibility with Adobe Express Add-ons API.

4. Local Testing

Set up a local SSL server for testing within Adobe Express:npx @adobe/ccweb-add-on-ssl setup --hostname localhost
npm run start


Tested the add-on directly in Adobe Express to ensure seamless integration and chat functionality.

5. Build for Production

Built the final bundle for deployment:npm run build


Output files were bundled into the /dist folder, ready for submission to the Adobe Add-ons Marketplace.

🔧 Built With

Adobe Express Add-ons API
Google Gemini 1.5 Flash (Generative Language API)
TypeScript
JavaScript / HTML / CSS
Node.js
@adobe/ccweb-add-on-scripts


🧠 Example Prompts

"Suggest a modern layout for a fashion flyer"
"Write a caption for an Instagram post about mental health awareness"
"Give me 3 ideas for a startup product hero section"


📈 Roadmap

Add canvas context awareness (e.g., selected elements)
Auto-suggest design edits or templates
Launch publicly in Adobe Add-ons Marketplace
Enable voice-to-text or custom model options


🪪 License
This project is licensed under the MIT License — use, fork, and contribute freely.

📹 Demo & Screenshots
Coming soon — demo video and usage preview will be uploaded after Devpost submission.

💻 Installation

Clone the repository:git clone https://github.com/your-username/luminara-ai.git


Navigate to the project directory:cd luminara-ai


Install dependencies:npm install


Initialize the project template (if starting fresh):npx @adobe/create-ccweb-add-on design-chat-addon --entrypoint panel --template javascript


Set up local SSL server for testing:npx @adobe/ccweb-add-on-ssl setup --hostname localhost


Start the development server:npm run start


Build for production:npm run build




🤝 Contributing
Contributions are welcome! Please read the contributing guidelines for details on how to get started.

Fork the repository
Create a feature branch (git checkout -b feature/your-feature)
Commit your changes (git commit -m 'Add your feature')
Push to the branch (git push origin feature/your-feature)
Open a pull request


📬 Contact
For questions or feedback, reach out via GitHub Issues or contact the team at your-email@example.com.

✨ Luminara.ai — Because creativity should never hit pause.
