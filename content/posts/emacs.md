+++
date = '2025-04-02T09:40:51+02:00'
draft = false
title = 'Getting started with Emacs'
+++

## What is Emacs?
Have you ever wished for a tool that adapts perfectly to your workflow, whether you're coding, writing, or managing complex projects?
Emacs isn’t just a text editor—it's a powerhouse that evolves with your needs.
From its customizable interface to its vast array of features, Emacs has become the go-to choice for developers, writers, and power users who want complete control over their environment.
Whether you're tackling a simple task or navigating an intricate coding project, Emacs has the flexibility to do it all—and more.
<!--more-->

In this blog post - written entirely in Emacs - I'm going to introduce the major features of the editor.

## Installing Emacs
Before we dive into the details, I encourage you to install Emacs on your system.
You can find the installation instructions for various platforms [here](https://www.gnu.org/software/emacs/download.html).

## Configuring Emacs
But to really get started with using Emacs, we have to do some work upfront.
To truly harness the power of Emacs, you'll want to customize it to your needs.
If you’re already familiar with Vim and prefer its keybindings, Emacs makes it easy to replicate them through a minor mode called Evil-Mode.
Evil-Mode allows you to use Vim-style keybindings inside Emacs.

By default, Emacs uses a different set of keybindings and if you would like to learn them instead, that's totally valid as well.
Since I don't know those myself, I'll stick to Evil-Mode and its keybindings.

To enable it, you'd need to install this package first.
Emacs provides several ways of doing it.
Feel free to use my personal configuration for Emacs, which includes Evil-Mode and many other customizations.
You can find it on my GitHub repository: https://github.com/johannes-el/emacs-dotfiles.

To use my configuration, clone the repository and rename the folder to .emacs.d in your home directory.
You can do this by running the following shell script:
```bash
#!/usr/bin/bash

git clone https://github.com/johannes-el/emacs-dotfiles --depth=1

if [ -d "$HOME/.emacs.d" ]; then
    rm -rf "$HOME/.emacs.d"
fi

mv emacs-dotfiles "$HOME/.emacs.d"
```

If you're looking for a more stable and polished starting point, consider checking out [Doom Emacs](https://github.com/doomemacs/doomemacs) or [Spacemacs](https://github.com/syl20bnr/spacemacs).
As you've likely noticed, a well-crafted configuration can significantly enhance your experience compared to using vanilla Emacs.

## Features
### Documentation
The following list of features does not claim to be exhaustive. It tries to showcase how powerful Emacs is and introduces the most used packages.

The first notable thing about Emacs is that it is self-documenting, meaning all of the functionality Emacs provides is built right into the editor itself.
This makes it really easy to look things up when you want to learn about new functionalities.

### Magit
If you've done any kind of version control, you must have come across Git.
Magit is a full-blown Git-procelein integrated into Emacs.

What makes Magit so powerful is its incredible ease of use. In a typical shell, you're likely accustomed to running commands like ```git add .``` or ```git commit -m "commit message"``` repeatedly.
Magit streamlines this process by covering the vast majority of Git commands, all accessible through simple shortcuts.
Its intuitive interface draws you in, making it a joy to use—once you're in the buffer, you’ll find yourself wanting to stay there and explore its full potential.
Magit also excels at displaying diffs, offering a clean and efficient interface that enhances the experience.
It is one of the most powerful packages in Emacs, and I highly recommend using it, as it will yield significant benefits in the long run.

### Org-mode
Org-mode is a powerful, flexible, and highly customizable major mode in Emacs designed for organizing and managing notes, tasks, and projects. 
You can create to-do lists, track deadlines and much more.
It is commonly used for note-taking and allows you to keep track of information easily.
Agenda view provides a comprehensive agenda that aggregates tasks and deadlines, helping you stay on top of your schedule.
Org-mode allows exporting your documents to various formats like HTML, PDF, LaTeX, Markdown (via pandoc), making it useful for creating reports, documents, or presentations.
Org-mode also supports inline code execution, which is one of its standout features.

### Org-roam
Org-roam allows users to craft their own personal wiki (often referred to as their second brain).
It identifies .org-files with unique IDs and let's you navigate code quickly.
The major selling point of Org-roam is that you can build your own Zettelkasten inside Emacs.
You can even visualize your notes with a frontend, allowing you to explore the Zettelkasten further: https://github.com/org-roam/org-roam-ui.

### Gnu Emms
The Emacs Multimedia System (EMMS) lets me play music directly from external players like mpv, which creates a fun and immersive experience.
Personally, I store all my music files in a directory that EMMS defaults to when launched.
This allows me to jump straight into an EMMS buffer and enjoy my favorite tunes without missing a beat.

### ERC
ERC is an IRC client in Emacs. I use it frequently myself to talk to fellow Emacs users all things Emacs!

### Projectile
Projectile is a project interaction library for Emacs. It allows you to seperate your code into projects and also ships with powerful tools like projectile-grep.

### Notmuch
Notmuch is a package for indexing Mails in Emacs.
When combined with a command-line utility like mbsync (which synchronizes mail between an IMAP server and a local mail directory),
you can easily read all your Mails in Emacs.

### Open Source
Emacs is Open Source and you can modify it to your own liking.
I really enjoyed making my own configuration and I encourage you to do the same!

## Conclusion
There is a lot more to Emacs than what is covered in this article, but by now you should have a broader view on what Emacs is capable of doing.
For me, Emacs is the most pleasant computing experience you can have and I'd be happy if I convinced any reader to join the Church of Emacs!