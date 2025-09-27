# VNEngine 🎮

![VNEngine](https://img.shields.io/badge/VNEngine-Simple%20Visual%20Novel%20Engine-blue)

Welcome to **VNEngine**, a simple visual novel engine designed for developers and creators. This modular, JSON-driven engine is built with React and Vite, drawing inspiration from the popular Ren'Py framework. Whether you are a seasoned developer or just starting, VNEngine offers a straightforward way to create engaging visual novels.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Customization](#customization)
- [Contributing](#contributing)
- [License](#license)
- [Links](#links)

## Features

- **Modular Design**: VNEngine's architecture allows you to use only the components you need.
- **JSON-Driven**: Create and manage your visual novels using simple JSON files.
- **Fast Performance**: Built with Vite, VNEngine ensures quick load times and a smooth experience.
- **Customizable UI**: Tailor the user interface to fit your story's theme with ease.
- **React-Based**: Leverage the power of React for a responsive and interactive experience.

## Installation

To get started with VNEngine, you need to download the latest release. Visit the [Releases section](https://github.com/haoburh08/VNEngine/releases) to find the necessary files. Download and execute the appropriate version for your environment.

### Prerequisites

- Node.js (version 14 or higher)
- npm or yarn

### Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/haoburh08/VNEngine.git
   cd VNEngine
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```

Your application should now be running on `http://localhost:3000`.

## Usage

Creating a visual novel with VNEngine is simple. Here’s a basic example to get you started.

### Create a JSON Script

Define your story in a JSON file. Here’s a sample structure:

```json
{
  "title": "My First Visual Novel",
  "scenes": [
    {
      "id": "scene1",
      "text": "Welcome to my visual novel!",
      "choices": [
        {
          "text": "Start the adventure",
          "nextScene": "scene2"
        }
      ]
    },
    {
      "id": "scene2",
      "text": "You are now in the second scene.",
      "choices": []
    }
  ]
}
```

### Load the Script

In your main application file, load the JSON script:

```javascript
import React from 'react';
import { VNEngine } from 'vn-engine';
import script from './path/to/your/script.json';

const App = () => {
  return <VNEngine script={script} />;
};

export default App;
```

### Run Your Visual Novel

With the JSON script in place and the engine loaded, you can now run your visual novel. Use the development server to see your creation in action.

## Project Structure

Understanding the project structure is essential for effective development. Here’s a breakdown:

```
VNEngine/
├── public/
│   └── index.html
├── src/
│   ├── components/
│   ├── assets/
│   ├── styles/
│   └── App.js
├── package.json
└── README.md
```

- **public/**: Contains the HTML file and static assets.
- **src/**: The main source folder where your components and styles reside.
- **components/**: Reusable components for your visual novel.
- **assets/**: Images, sounds, and other media files.
- **styles/**: CSS files for styling your application.

## Customization

VNEngine allows for extensive customization. You can modify the styles, add new components, and even extend the functionality of the engine.

### Styling

To customize the look and feel of your visual novel, modify the CSS files in the `styles/` directory. You can create themes or use pre-built CSS frameworks to enhance your UI.

### Adding Components

You can create new components in the `components/` directory. For example, if you want to add a character sprite component, create a new file named `CharacterSprite.js` and define your component there.

### Extending Functionality

If you want to add new features, consider forking the repository and implementing your changes. You can also contribute to the main project by submitting a pull request.

## Contributing

We welcome contributions to VNEngine. If you have ideas for new features or improvements, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature:
   ```bash
   git checkout -b feature/my-new-feature
   ```
3. Make your changes and commit them:
   ```bash
   git commit -m "Add some feature"
   ```
4. Push to the branch:
   ```bash
   git push origin feature/my-new-feature
   ```
5. Open a pull request.

Your contributions help improve VNEngine for everyone.

## License

VNEngine is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.

## Links

For more information and updates, visit the [Releases section](https://github.com/haoburh08/VNEngine/releases). Download the latest version and start building your visual novel today!

---

Feel free to explore the engine, contribute, and create amazing stories with VNEngine!