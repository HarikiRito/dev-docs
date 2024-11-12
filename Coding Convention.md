# Coding Convention

This topic is quite broad since every person has their own coding conventions based on their preferences. But to be honest, not everyone's convention is good, at least in my experience. I have worked on many projects, ranging from small to big, from simple to complex, with a variety of programming languages and technologies, and yet I still have to master my own coding conventions continuously.

You might ask: Why don't you just have a common convention for the specific team and project and leave it at that? Well, the answer is simple: **There is no one-size-fits-all convention**. Also, as I said above, people have different preferences, and you don't know how many times someone on my team has found a way to get around the convention that I have set up in the CI/CD pipeline. They can find interesting ways to bypass the convention, and I praise them for being so creative in spotting loopholes. Then, I have to fix it again and again.

No more chit-chat; let's get into the topic.

# 1. Naming Convention

This is pretty straightforward. I'm going to say: follow the convention of the programming language or the framework that you are using. For example, if you are using TypeScript, follow the TypeScript naming convention. The same applies to other languages and frameworks. The reason is simple: the language or framework you are using must already come with a naming convention that is well-known and accepted by the community. Therefore, if you follow it strictly, there is a good chance that when you are working with other people, they will understand your code better since they are familiar with the naming convention of the programming language. Here is the secret: **I prefer camelCase, but I don't mind if the project uses snake_case or kebab-case**.

# 2. Formatting

This is the same as the naming convention. You could use whatever formatting you and your team agree on. You only need to be consistent with the formatting. Otherwise, things will get messy pretty quickly when you have many people working on the same project. Usually, each language comes with a formatting tool that is already batteries-included. For example, `TypeScript` has `prettier,` `Go` has `gofmt,` `Dart` has `dartfmt,` etc. These are the languages that I have worked with, and I'm sure that if your language isn't included here, your language of choice will have at least one tool for formatting. They often come with customization options, so you can adjust them to your liking. In conclusion, **you only need to be consistent with the formatting**.

# 3. Code Comments

Normally, I don't like to write comments in the code. I believe that the code should be self-explanatory. If you have complicated logic, you should break it down into smaller functions with descriptive names. If you have complicated logic that you think needs a comment, you should probably refactor the code to make it more understandable. But there is always an exception to the rule, for example, if you are working on a legacy project or if the function or class is doing something that is far too complicated to be understood by someone just by reading the code. In that case, you should write comments to explain the logic.




# 4. How to name things properly

This is why I said that comments are not that important to me. Just name things properly, making the code self-explanatory. For example, do not shorten the variable name to something like `a, `b,` `c,` etc. Make it descriptive. One use case that I see a lot is that people will use `i' as the index of the loop. Is writing out the for loop so complicated that you have to shorten the variable name to `i'? I know there are some courses on the internet that teach you to name the variable as `i' for the index of the loop, but remember, you're going to be working with other people, and what happens if you have another loop nested inside the first one? Others need to understand your code, and they will thank you if you name things properly rather than checking the code commit history to figure out what the hell `a, `b`, and `c` mean.

# 5. Code Structure

The code structure is the core of the project. If the project is organized properly, adding new features will be a breeze. There are currently two ways that I know of as of this writing: `Feature-based architecture` and `Layer-based architecture`. You can read more about them [here](https://medium.com/sahibinden-technology/package-by-layer-vs-package-by-feature-7e89cde2ae3a).

### Layer-based architecture
You might be more familiar with `Layer-based architecture` since this is what we taught in school. Remember the `Model,` `View,` and `Controller` patterns? This is what I'm talking about. MVC is one of the most popular layer-based architectures among developers.
It can be found in many popular frameworks, such as `Spring Boot` for `Java,` `Laravel` for `PHP,` etc. Basically, the idea is to separate the code into different layers, and each layer holds a list of files that are related to the layer. For example, the `Model` layer will hold the `Model` files, the `View` layer will hold the `View` files, and the `Controller` layer will hold the `Controller` files. This makes the code more organized and easier to understand. However, the problem with this approach is that when the project grows bigger, and you need to add a new feature, you will find it hard to find the files that are responsible for the feature.

### Feature-based architecture
By declaring each feature and its related files in the feature folder, you can easily find the files that are responsible for the feature. For example, grouping both the `Model,` `View,` and `Controller` files in the same feature folder. This way, each feature is isolated from the others, thus increasing `encapsulation.` The feature is considered a `module,` which can be used without worrying that it will affect other features. Imagine it is like a LEGO block, where each block can be combined to form a complete product. This way, adding more features is a breeze, while you can still maintain the code that already exists since you can ensure that the newly added feature will not affect the existing code in a negative way.