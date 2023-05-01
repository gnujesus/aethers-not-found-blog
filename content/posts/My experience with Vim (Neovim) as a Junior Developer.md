---
title: "My experience with Vim (Neovim) as a Junior Developer"
date: 2023-04-28T08:43:14-04:00
draft: false
description: 'My experience using Neovim on my journey to become a senior developer'
tags: ['GitHub', 'Hugo','complaints', 'static website', 'front-end']
keywords: 
- Aether
- GitHub
- Hugo
- Static Site
- HTML
- CSS
- Web Development
- Programming
- Tech
categories: ['Blog', 'Personal']
---

# Introduction

I first learned about Vim thanks to [ThePrimeagen](https://www.youtube.com/@ThePrimeagen), a software developer and engineer who works at Netflix btw. When I saw Vim in action in the hands of an expert, coding in the exact same language I was learning in that moment but at the speed of light, made me realize that I couldn’t live my life as a developer without learning Vim. 

The shortcuts, the customization, the feel of control, the power, but overall… ********************the speed.******************** I first spent some days doing my respective research about the topic, but I eventually hopped into it without even noticing. 

# What is Neovim

Is the best editor there is. Jk.

Vim is a modal, free open-source text editor. It was first released for UNIX, and is (as you may guess) the text editor that comes by default with Linux. Neovim is aimed to improve text editing by the usage of keybindings, which gives users a more homerow-centric experience when it comes to code.

Neovim is actually a fork from which adds functionalities and improves some things about the editor.

# Why is Neovim better than every other code editor

## Blazingly Fast

Disclaimer: I will be referring to Vim (the program) as Neovim, since that’s what I use and prefer, but will refer to Vim (the keybindings) as Vim.

Neovim offers a plethora of keybindings which allows programmers to speed up the process of developing a program, as well of a library even bigger of plugins that offers customization settings for improvement in any area of text editing. It’s like Atom: “**********************A hackable code editor**********************”, but this is actually a hackable code editor. RIP Atom btw.

Say for example that you want to delete a specific number of lines of code because you have to rewrite them for refactoring purposes. In Vscode, you would have to do one of these two things:

- **Option 1**: Move your hand from your keyboard to your mouse (or mousepad if you’re completely out of your mind), then grab it, select the lines you want to delete, move your hand to your keyboard again and then press either `backspace` or `enter`.
- ********************Option 2:******************** Press `Shift`, press the up arrow until you have selected all the lines, and then `backspace` or `enter`.

As you see, this is a process that takes too long to perform using normal keyboard bindings, but Vim keybindings are magic.

Say the number of lines that are to be deleted is 8. Using Vim, you only have to do the following: `Shift-V 8-k-d`. That’s what I call blazingly fast.

With only knowing what each key does, and what each combination does, the process of deleting some lines has shortened by an eternity. But that’s only a little demonstration of the many cases in which Vim has helped me shorten the process of doing multiple tasks that would’ve taken me forever, like editing code inside a pair of specific brackets.

Let’s illustrate another example, you’re coding in TypeScript (because we all know JavaScript sucks) and you need to edit the anonymous function on the event listener which is located inside a for loop. That would look like this:

```tsx
const buttons = document.querySelectorAll('.circle');

for (let i = 0; i < buttons.length; i++){
	buttons[i].addEventListener('click', function(){
		console.log('Hello World');
	}
}
```

Here we have two pairs of brackets, let’s say that you want to change the `console.log()` for a `if` statement. Using Vscode you would have to grab your mouse again, move into the brackets, select, delete and edit, or use you keyboard arrows which is, honestly, more suffering in this case.

Using Vim you only have to place yourself inside or near the brackets using `hjkl`, and then `c i {` into those sissy brackets and edit your code. Again, blazingly fast. This combination of keys will place you inside the nearest brackets and delete whatever’s inside of them, and put you on input mode so you can introduce text.

## Customization

Neovim allows it’s users to customize it to the core. After installing it, it comes as a plain text editor without more than basic text editing functions, and commands and combinations of keys that facilitate the code editing process (take into account that I’m not a Vim professional, I may be missing something here).

It has a wide community of users who develop and are constantly updating plugins for it’s optimal usage, which allows you to customize it in ways you may have never imagined.

## Wide Community

Neovim has a wide community of users who offer support for the many features included in Neovim, as well as support for it’s plugins and instructions on how to use these properly to avoid or troubleshoot any mistakes. 

Either it is on GitHub, StackOverflow, Discord, ThePrimeagen’s YouTube channel, Tpope’s twitter, my blog, Google, ChatGPT, you can be sure that you will always find support and instructions about almost anything you can think of about Neovim’s usage.

# Why you shouldn’t use Neovim if you’re just starting to code

I’ll say this straight: setting up Neovim takes time, and learning how to set everything up and understand how things work takes even longer. If you’re just starting to code, I recommend downloading the Vim plugin for your text editor, or enabling the Vim keybinding if your text editor has those included. 

As a Neovim user, I have to admit that I have gone through heaven and hell trying to create my own configuration for the editor, either trying to set it up or dealing with errors that pop up from nothing while trying to print ‘hello world’ on Brainfuck.

The time you spend into setting up Neovim could be used to learn how to really use Vim shortcuts, and this can be done perfectly using Vscode. Even better, the time spent trying to understand how to set up Neovim could be used to actually learn how to code, work on projects and improve your programming ability. I’m not saying you should forget about switching to Neovim as your editor, but it is important that you evaluate what’s urgent and what’s important. I would advice you that if you’re planning on understanding how to configure Neovim and how everything works, take some time to learn the fundamentals of Lua, it will make the process way easier.

# Summary

Neovim is a fantastic code editor which may suit the workflow of many people, and help speed up the coding process of code and text editing. It's the perfect code editor for those adept to freedom and capability of customization and, in the long term, it's definitely going to be useful. 

However, if you're just starting to learn how to code, I don't recommend learning how to set up Neovim, but rather learning Vim keybindings if your code editor includes a plugin for this or a Vim mode by default.

# Conclusion

Vim > Vscode.