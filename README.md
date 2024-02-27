# Team Chat Application

## Description

This project is a comprehensive team chat application modeled after Discord's capabilities but tailored for organizational use. It's designed with modern technologies to provide real-time messaging, multimedia sharing, various communication channels, and advanced user management. The goal is to create a scalable and user-friendly platform for effective team collaboration.

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Repository Structure](#repo-struct)
- [Contributing](#contributing)
- [License](#license)
- [Authors](#authors)
- [Acknowledgments](#acknowledgments)

## Features

- Server creation and management for organizing team communication.
- Real-time text messaging with options for editing and deletion.
- Media attachments in conversations.
- Text, video, and audio channels for communication.
- Dark and light mode for user interface customization.

## Technologies

- **Next.js 13**: For server-side rendering and static site generation.
- **React**: For building the user interface components.
- **Socket.io**: For real-time communication between clients and servers.
- **Prisma**: For database interactions and ORM.
- **Tailwind CSS**: For styling and customizing the application's look and feel.
- **MySQL (Planetscale)**: As the relational database for data storage.
- **Clerk**: For user authentication and security.
- **Chakra UI**: For building a consistent and accessible user interface.

## Repository Structure

```plaintext
Directory information : 

CSCE-5430.400-Group-7/
├── source-code(team-chat-app)/             # Contains all application source code
│   ├── components/          # Reusable UI components
│   │   ├── Chat/            # Components related to chat functionality
│   │   ├── UI/              # Generic UI components like buttons, modals, etc.
│   │   └── Layout/          # Components for layout and structure
│   ├── pages/               # Next.js pages directory
│   │   ├── api/             # API routes
│   │   └── [page].js        # Application pages
│   ├── public/              # Static files like images and icons
│   ├── styles/              # Tailwind CSS files and custom styles
│   ├── prisma/              # Prisma schema and migrations
│   ├── utilities/           # Utility functions and hooks
│   ├── lib/                 # Library for shared functions and middleware
│   ├── hooks/               # React custom hooks
│   ├── context/             # React context for state management
│   ├── models/              # Data models for Prisma
│   ├── server/              # Server-side logic and Socket.io setup
│   ├── scripts/             # Scripts for development and deployment
│   └── __tests__/           # Unit and integration tests
├── Group-Info               # Information about the project team
├── meeting minutes/         # Records of team meetings
├── planning documents/      # Initial and ongoing planning documents
└── project reports/         # Deliverable Reports
│   ├── Group-7-del-1.pdf/   # Deliverable 1 document (name : Group-7-del-1.pdf)
│   ├── Deliverable-2.pdf/   # Deliverable 2 document (name : Deliberable-2.pdf)
└──note-deliverable1.txt/    # Directory information for deliverable 1
└──note-deliverable2.txt/    # Directory information for deliverable 2

```

## Contributing

We encourage contributions from everyone. If you're interested in helping out, please read our [Contributing Guide](CONTRIBUTING.md).

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Authors

- **Srichandan Kota** - *Project Lead* - [SrichandanKota](https://github.com/SrichandanKota)
- **Swapna Sonti** - *Frontend Developer* - [SwapnaSonti](https://github.com/SwapnaSonti)
- **Sandeep Chowdary Ari** - *Backend Developer* - [SandeepAri](https://github.com/SandeepAri)
- **Venkata Sai Shankar Koppula** - *UI/UX Designer* - [VenkataKoppula](https://github.com/VenkataKoppula)
- **Shivanandha Reddy Vasudevula** - *Database Administrator* - [ShivanandhaVasudevula](https://github.com/ShivanandhaVasudevula)
- **Gana Deekshith** - *Authentication Lead* - [GanaDeekshith](https://github.com/GanaDeekshith)
- **Kantumutchu Dinesh** - *UI Developer* - [KantumutchuDinesh](https://github.com/KantumutchuDinesh)
- **Bhanu Prasad Krishna Murthy** - *Documentation Lead* - [BhanuMurthy](https://github.com/BhanuMurthy)

## Acknowledgments

- A shoutout to all the open-source projects that made this application possible.
- Thanks to our team members and contributors who have invested their time and effort into this project.

## Contact Information

For any queries or support, please contact us at [SrichandanKota@my.unt.edu](mailto:SrichandanKota@my.unt.edu).
```
