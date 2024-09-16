# 🌟 Rules to Live By

Here are some rules of thumb, heuristics, and principles that you might find useful in your career as a software developer:

1. Less code is better than more code. No code is best of all.
2. Run the code as you write it.
3. If you've done the same thing four times, automate it.
4. Everything is a trade-off. There is no free lunch.
5. A user and a developer will use the same code differently.
6. Choose portability over efficiency.
7. Build a prototype as soon as possible.
8. If it works first time, be suspicious.
9. Think in type systems, even when you're not programming in a typed language.
10. Algorithms are science, software is art.

# 1. Less code is better than more code. No code is best of all.

Every line of code you write is a line of code you have to maintain.
Every line of code you write is a line of code that can have bugs.
Every line of code you write is a line of code that can be misunderstood and misused.
Code is a liability, not an asset!

However, be wary of oversimplifying to the point of obfuscation.
Sometimes, a bit more code can significantly enhance readability and maintainability.
For instance, explicit code in Python, even if slightly longer, is often preferred over cryptic one-liners for clarity.

Strive for simplicity and elegance; often, the most powerful solution is the most understated.

# 2. Run the code as you write it.

Don't write a whole bunch of code and then try to run it.
Write a little bit of code, and then run it.

This is especially true when you're learning a new language or framework.
But it's something you should do all the time.

It's much easier to debug a small amount of code than a large amount of code.
And it's also much easier to solve a problem while the code is still fresh in your "brain RAM".

Adopting this habit leads to a more efficient development process and helps in maintaining a clear understanding of the code's behavior at each step.
Early and frequent testing prevents the accumulation of bugs and reduces the complexity of troubleshooting.

But it's important to balance between testing small pieces and understanding the bigger picture.
Sometimes, focusing too much on small increments can lead to missing out on architectural flaws or bigger design issues.

# 3. If you've done the same thing four times, automate it.

If you've done the same thing four times, you're probably going to do it again.
And as a rough heuristic, automating something takes about four times as long as doing it manually.
So if you've done the same thing four times, it's probably worth automating!

Embrace this as a catalyst for innovation and efficiency.
Automation not only saves time but also reduces errors, freeing you to focus on more complex and creative tasks.

Of course, sometimes the effort to automate a task can outweigh its benefits, especially if the task evolves frequently or is too complex.

# 4. Everything is a trade-off. There is no free lunch.

A more efficient algorithm probably means more complex code.
A better user experience probably means more code to write and maintain.
A more portable program probably means a slower program.
A more secure program probably means a less usable program.

There is no hard and fast rule here. Often decisions involve matters of opinion that lead to heated debates.
But it's important to remember that everything is a trade-off.
There is no such thing as a perfect solution.

In every decision, seek balance. Prioritize based on the context and goals.
Recognizing and managing these trade-offs is a hallmark of great engineering.

It's equally important to contextualize these trade-offs within the specific requirements of a project.
For instance, in high-performance computing, efficiency might take precedence over portability.

# 5. A user and a developer will use the same code differently.

A user will use your code in ways you never imagined, intended or wanted.

It's very difficult for us as developers to visualise how a user with no knowledge of the internals of our code will use it.
Because we know how it works, we use it in exactly the way it was intended.

This underscores the importance of designing with empathy and robustness.
Always expect the unexpected and design for it.
Our code should be as intuitive as it is functional.

But again, balance!
Overemphasizing user flexibility can sometimes lead to overly complex code structures.

# 6. Choose portability over efficiency.

A more portable program might well mean making concessions in terms of efficiency and what technologies you can use.
However, a brilliant program is no good if the user can't run it.

Web technologies are a great way to build portable programs.
And with the advent of WebAssembly, you can even run programs written in other languages in the browser.
WebGPU is also on the horizon, which will allow you to write high-performance graphics code in the browser!

Remember, the reach and accessibility of our software often trump raw performance.
Strive to build software that is inclusive and available to a wider audience, leveraging emerging technologies to bridge gaps in efficiency.

It's quite rare that in the commercial world, you need to squeeze every last drop of performance out of your code.
But it may happen.
If it does, you can always rewrite the performance-critical parts in a lower-level language like C or Rust.

# 7. Build a prototype as soon as possible.

It's unlikely we know what all the hurdles are going to be until we get our hands dirty.
And a prototype is a great way to test our ideas and get feedback from users.

Building an minimal viable product (MVP) is how we can quickly validate our ideas and get a sense of what works and what doesn't.

Embrace the iterative process; each prototype iteration brings clarity and refinement. This approach not only saves time and resources but also keeps the project aligned with user needs and market demands.

Rapid prototyping is essential, but it's important not to rush into building without sufficient planning.
Sometimes, spending extra time in the design phase can save considerable time later by avoiding major reworks.

# 8. If it works first time, be suspicious.

I always get nervous when my code works first time.
Perhaps it comes from when we first learn to program, and things are more often broken than not.
But I think it's a good rule of thumb to be suspicious of code that works first time.

As we become more experienced we get better at writing code, but we may also become more complacent.

Always double-check and rigorously test your code, even when it seems to work perfectly.
This practice is not about doubting your skills but ensuring quality and reliability.
The best developers know that the devil is often in the details, and that thorough validation is key.

# 9. Think in type systems, even when you're not programming in a typed language.

Even if you're not programming in a typed language, it's still useful to think in terms of types.
Whilst we won't know the specific values going through the pipe, we should still have a good idea of what _type_ of data we're dealing with.

If we're building an API, or a library, or a framework, we should be thinking about the types of data that are going to be passed in and out of our code.
This way other developers can write code that will interface with ours - even if it's not built yet!

Considering types enhances the clarity, maintainability, and interoperability of your code.
It's about anticipating how your code interacts with other parts of the system and ensuring that these interactions are as smooth and error-free as possible.

However, it's also important to leverage the strengths of dynamically typed languages where appropriate, as they can offer flexibility and speed in development.

# 10. Algorithms are science, software is art.

Baking is a science, cooking is an art.

Baking is a science because you have to follow the recipe exactly.
You mix the ingredients, and then you put them in the oven for a certain amount of time at a specific temperature, and then hopefully a beautiful cake comes out.

Cooking is an art because you can improvise.
Nay, you must improvise!
You taste as you go, and you adapt as the dish develops.
If the sauce is too bland, you add more salt.
If the sauce is too thin, you add more flour.
If things start to burn, you turn down the heat.
The evolving nature of the dish means that you often don't follow the recipe to the letter.
You interpret it, and you adapt it to your own tastes.

Developing algorithms is a science, developing software is an art.

An algorithm's objectives are usually well defined and unambiguous - often to maximize speed and/or minimize memory usage.

However, a complete program is often too complex to be approached in the same way.
There are many more moving parts to consider, and the "objectives" are often more "subjective".

Your role as a developer is not only to construct efficient algorithms but also to sculpt a software architecture that anticipates and accommodates future changes, growth, and challenges.

# Recap

1.  **Less code, more impact**: Every line of code is a potential bug. Striving for simplicity is key. In Python, the Zen of Python[^note] emphasizes readability and simplicity, a testament to this principle.
2.  **Iterative development**: Running code as you write is crucial. Tools like Jupyter notebooks for Python and REPL environments in languages like JavaScript foster this practice. It aligns well with the agile development approach.
3.  **Automation is your ally**: The automation principle is a cornerstone of modern DevOps practices. Using tools like Ansible for automation, or writing custom scripts in Python, can save immense amounts of time.
4.  **Trade-offs are everywhere**: This is a core concept in software architecture. The balance between scalability, performance, and maintainability is always a juggling act.
5.  **Design for the user**: Understanding the user's perspective is crucial. This is where user stories and personas in agile methodologies become valuable.
6.  **Portability vs. Efficiency**: Web technologies like React (JavaScript) and WebAssembly for more performance-intensive tasks are reshaping how we think about portable software.
7.  **Prototype early**: MVPs (Minimum Viable Products) and rapid prototyping are vital in today's fast-paced tech environment. Tools like Flask for Python provide a quick way to get a web server running for prototyping.
8.  **Healthy skepticism**: A "too good to be true" scenario often is. Rigorous testing and validation, maybe using Python's `unittest` or JavaScript's `Jest`, are essential.
9.  **Type systems**: Even in dynamically typed languages like Python, type hinting (PEP 484) has gained traction. It improves readability and maintainability.
10. **Art and science of coding**: This beautifully captures the essence of software development. It's not just about solving problems but about how elegantly and sustainably you solve them.

[^note]: Put `import this` in your script/REPL to get this Easter Egg:

```shell
The Zen of Python, by Tim Peters

Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!
```