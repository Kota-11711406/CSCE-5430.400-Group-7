# Team Chat Application

## Description

This project is a comprehensive team chat application. It's designed with modern technologies to provide real-time messaging, multimedia sharing, various communication channels, and advanced user management. The goal is to create a scalable and user-friendly platform for effective team collaboration.

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
├── meeting minutes\                                # Directory for meeting minutes
│   ├── Meeting Minutes - Deliverable 2.pdf
│   ├── Meeting Minutes - Deliverable 3.pdf
│   └── Meeting Minutes-Deliverable 1.pdf
│
├── planning documents\                              # Directory for planning documents
│   └── Planning document.pdf
│
├── project reports\                                  # Directory for Deliverable reports
│   ├── .DS_Store
│   ├── Deliverable-2.pdf
│   └── Group-7-del-1.pdf
│   └── Deliverable-3.pdf/            
│
├── team-chat-app-sourceCode-Phase1(source-code)\                                  # Main directory for the team chat application
│   │
│   ├── app\                                        # Contains the core application files
│   │   │
│   │   ├── (auth)\
│   │   │   │
│   │   │   ├── (routes)\
│   │   │   │   │
│   │   │   │   ├── sign-in\
│   │   │   │   │   │
│   │   │   │   │   └── [[...sign-in]]\
│   │   │   │   │       └── page.tsx
│   │   │   │   │
│   │   │   │   │
│   │   │   │   └── sign-up\
│   │   │   │       │
│   │   │   │       └── [[...sign-up]]\
│   │   │   │           └── page.tsx
│   │   │   │
│   │   │   │
│   │   │   │
│   │   │   └── layout.tsx
│   │   │
│   │   ├── (invite)\                                 # Routes for invite functionality
│   │   │   │
│   │   │   └── (routes)\
│   │   │       │
│   │   │       └── invite\
│   │   │           │
│   │   │           └── [inviteCode]\
│   │   │               └── page.tsx
│   │   │
│   │   │
│   │   │
│   │   │
│   │   ├── (main)\                                # Main application components
│   │   │   │
│   │   │   ├── (routes)\
│   │   │   │   │
│   │   │   │   └── servers\
│   │   │   │       │
│   │   │   │       └── [serverId]\
│   │   │   │           │
│   │   │   │           ├── channels\
│   │   │   │           │   │
│   │   │   │           │   └── [channelId]\
│   │   │   │           │       └── page.tsx
│   │   │   │           │
│   │   │   │           │
│   │   │   │           ├── conversations\
│   │   │   │           │   │
│   │   │   │           │   └── [memberId]\
│   │   │   │           │       └── page.tsx
│   │   │   │           │
│   │   │   │           │
│   │   │   │           ├── layout.tsx
│   │   │   │           └── page.tsx
│   │   │   │
│   │   │   │
│   │   │   │
│   │   │   └── layout.tsx
│   │   │
│   │   ├── (setup)\                                 # Setup related components
│   │   │   └── page.tsx
│   │   │
│   │   ├── api\                                     # API routes
│   │   │   │
│   │   │   ├── direct-messages\
│   │   │   │   └── route.ts
│   │   │   │
│   │   │   ├── members\
│   │   │   │   │
│   │   │   │   └── [memberId]\
│   │   │   │       └── route.ts
│   │   │   │
│   │   │   │
│   │   │   ├── messages\
│   │   │   │   └── route.ts
│   │   │   │
│   │   │   ├── servers\
│   │   │   │   │
│   │   │   │   ├── [serverId]\
│   │   │   │   │   │
│   │   │   │   │   └── invite-code\
│   │   │   │   │       └── route.ts
│   │   │   │   │
│   │   │   │   │
│   │   │   │   └── route.ts
│   │   │   │
│   │   │   └── uploadthing\
│   │   │       ├── core.ts
│   │   │       └── route.ts
│   │   │
│   │   │
│   │   ├── favicon.ico
│   │   ├── globals.css
│   │   └── layout.tsx
│   │
│   ├── components\                          # Reusable UI components
│   │   │
│   │   ├── chat\                             # Components related to chat functionality
│   │   │   ├── chat-header.tsx
│   │   │   ├── chat-input.tsx
│   │   │   ├── chat-item.tsx
│   │   │   ├── chat-messages.tsx
│   │   │   ├── chat-video-button.tsx
│   │   │   └── chat-welcome.tsx
│   │   │
│   │   ├── modals\                             # Modal components
│   │   │   ├── create-server-modal.tsx
│   │   │   ├── delete-message-modal.tsx
│   │   │   ├── initial-modal.tsx
│   │   │   ├── invite-modal.tsx
│   │   │   └── message-file-modal.tsx
│   │   │
│   │   ├── navigation\                        # Navigation components
│   │   │   ├── navigation-action.tsx
│   │   │   ├── navigation-item.tsx
│   │   │   └── navigation-sidebar.tsx
│   │   │
│   │   ├── providers\                         # Provider components
│   │   │   ├── modal-provider.tsx
│   │   │   ├── query-provider.tsx
│   │   │   ├── socket-provider.tsx
│   │   │   └── theme-provider.tsx
│   │   │
│   │   ├── server\                             # Server components
│   │   │   ├── server-channel.tsx
│   │   │   ├── server-header.tsx
│   │   │   ├── server-member.tsx
│   │   │   ├── server-search.tsx
│   │   │   ├── server-section.tsx
│   │   │   └── server-sidebar.tsx
│   │   │
│   │   ├── ui\                                 # Generic UI components
│   │   │   ├── avatar.tsx
│   │   │   ├── badge.tsx
│   │   │   ├── button.tsx
│   │   │   ├── command.tsx
│   │   │   ├── dialog.tsx
│   │   │   ├── dropdown-menu.tsx
│   │   │   ├── form.tsx
│   │   │   ├── input.tsx
│   │   │   ├── label.tsx
│   │   │   ├── popover.tsx
│   │   │   ├── scroll-area.tsx
│   │   │   ├── select.tsx
│   │   │   ├── separator.tsx
│   │   │   ├── sheet.tsx
│   │   │   └── tooltip.tsx
│   │   │
│   │   ├── .DS_Store
│   │   ├── action-tooltip.tsx
│   │   ├── create-server-modal.tsx
│   │   ├── emoji-picker.tsx
│   │   ├── file-upload.tsx
│   │   ├── mobile-toggle.tsx
│   │   ├── mode-toggle.tsx
│   │   ├── socket-indicator.tsx
│   │   └── user-avatar.tsx
│   │
│   ├── hooks\                                         # React custom hooks
│   │   ├── use-chat-query.ts
│   │   ├── use-chat-scroll.ts
│   │   ├── use-chat-socket.ts
│   │   ├── use-modal-store.ts
│   │   └── use-origin.ts
│   │
│   ├── lib\                                         # Library for shared functions and middleware
│   │   ├── conversation.ts
│   │   ├── current-profile-pages.ts
│   │   ├── current-profile.ts
│   │   ├── db.ts
│   │   ├── initial-profile.ts
│   │   ├── uploadthing.ts
│   │   └── utils.ts
│   │
│   ├── pages\                     # Next.js pages directory
│   │   │
│   │   └── api\
│   │       │
│   │       └── socket\
│   │           │
│   │           ├── direct-messages\
│   │           │   ├── [directMessageId].ts
│   │           │   └── index.ts
│   │           │
│   │           ├── messages\
│   │           │   ├── [messageId].ts
│   │           │   └── index.ts
│   │           │
│   │           └── io.ts
│   │
│   │
│   │
│   ├── prisma\                    # Prisma schema and migrations
│   │   └── schema.prisma
│   │
│   ├── public\                   # Static files like images and icons
│   │   ├── next.svg
│   │   └── vercel.svg
│   │
│   ├── .DS_Store
│   ├── .eslintrc.json
│   ├── .gitignore
│   ├── README.md
│   ├── components.json
│   ├── middleware.ts
│   ├── next.config.js
│   ├── package-lock.json
│   ├── package.json
│   ├── postcss.config.js
│   ├── tailwind.config.js
│   ├── tailwind.config.ts
│   ├── tsconfig.json
│   └── types.ts
│
├── .DS_Store
├── Group-Info
├── README.md
├── note-deliverable1.txt
├── note-deliverable2.txt
└── note-deliverable3.txt

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
