# Lingo
  
[![Discord](https://img.shields.io/discord/1091306623819059300?color=7289da&label=Discord&logo=discord&logoColor=fff&style=for-the-badge)](https://discord.com/invite/m3TBB9XEkb)

> TLDR;  
> Lingo is a pseudo language designed to enhance Large Language Models (LLMs) like GPT-3 and GPT-4, providing a versatile syntax to guide more accurate outputs. Developed for the Hyv software development library, Lingo facilitates AI collaboration and efficient task management. Lingo's expressive syntax and extensible framework improve output quality and adaptability in various use cases.

Introducing Lingo, a powerful pseudo language designed to enhance the capabilities of Large Language Models (LLMs) like GPT-3 and GPT-4. Lingo provides a versatile syntax that enables users to define expectations and constraints, guiding LLMs to produce more accurate and contextually relevant outputs. Lingo has been developed as a perfect syntax for [Hyv](https://github.com/failfa-st/hyv), a modular software development library focused on AI collaboration. Hyv streamlines the development process by breaking complex tasks into manageable pieces and offers an adaptable design that works with various technologies. By using Lingo with Hyv, developers can harness the full potential of AI-assisted software development, fostering efficient task management and a paradigm shift in the field.

Large Language Models (LLMs) are a type of artificial intelligence model, specifically designed to process and generate natural language text. Among the most well-known LLMs are GPT-3 and GPT-4, developed by OpenAI. These models have achieved remarkable results in a variety of tasks, including text generation, summarization, translation, and question-answering. However, despite their impressive capabilities, LLMs may sometimes require guidance and constraints to produce contextually relevant and accurate outputs. This is where Lingo comes into play.

Lingo's syntax is highly extensible, allowing for the integration of new values and functions that adhere to its foundational principles. This flexibility ensures that Lingo remains adaptable to a wide range of tasks and use cases, making it an invaluable tool for working with LLMs.


## Key Features

-   **Expressive syntax**: Lingo's syntax is designed to be both concise and expressive, making it easy for users to define their requirements and for LLMs to interpret them accurately.
    
-   **Extensible and adaptable framework**: Lingo's syntax can be easily extended to incorporate new values and functions, allowing it to adapt to a wide range of tasks and use cases. This extensibility ensures that Lingo remains versatile and relevant as LLM technology advances and user requirements evolve.
    
-   **Improved output quality**: By providing LLMs with clear expectations and guidance, Lingo helps them generate more relevant and accurate outputs, reducing the need for manual fine-tuning or extensive user input.

By harnessing the power of Lingo, users can effectively guide LLMs to produce outputs that better align with their goals, while reducing the amount of manual intervention required. The extensible nature of Lingo's syntax ensures that it remains a valuable and relevant tool for working with LLMs, both now and in the future.


**Try it yourself**:

```
city: {
  name: "string",
  popultion: "int"
  poi: "string[] *<=3"
}
random(<=3{{city}}):json
```

![Screenshot 2023-05-08 at 17 28 26](https://user-images.githubusercontent.com/1148334/236865232-259fac97-e558-4ff5-9b60-f00da94b2841.png)

## Values

-   `{{key}}`: This is a placeholder for a variable or input value that will be replaced with actual content when used.

-   `~{{key}}`: The tilde (~) symbol is used to indicate an approximate value or range for the specified key. In this context, it means that the generated content should have a length close to the value of `key`.
    
-   `+{{key}}`: The plus (+) symbol is used to append or concatenate the value of `key` with another element. In this context, it means adding the specified property or attribute to the generated content.
    
-   `={{key}}`: The equals (=) symbol is used to indicate that the generated content should have an exact match or value equal to `key`.
    
-   `!{{key}}`: The exclamation (!) symbol is used to negate or exclude the value of `key` from the generated content. In this context, it means that the specified property or attribute should not be present in the output.
    
-   `-{{key}}`: The minus (-) symbol is used to remove or subtract the value of `key` from the generated content. In this context, it means excluding the specified property or attribute from the output.

-   `*{{key}}`: The asterisk (\*) symbol can be used to indicate that the generated content should repeat the specified property or attribute `key` times.
    
-   `>{{key}}`: The greater than (>) symbol can be used to indicate that the generated content should have a length greater than the value of `key`.
    
-   `<{{key}}`: The less than (<) symbol can be used to indicate that the generated content should have a length less than the value of `key`.

-   `<={{key}}`: The less than or equal to (<=) symbol is used to indicate that the generated content should have a length less than or equal to the value of `key`.
    
-   `>={{key}}`: The greater than or equal to (>=) symbol is used to indicate that the generated content should have a length greater than or equal to the value of `key`. 

-   `?{{key1}}:{{key2}}`: This syntax can be used for conditional expressions, where if the condition specified by `key1` is met, the generated content will include `key2`.

## Keywords
    
-   `ANY`: This keyword can be used to indicate that any of the specified conditions or constraints can be met in the generated content, not necessarily all of them.

-   `ALWAYS`: This keyword can be used to indicate that a specific condition or constraint should always be met in the generated content.

-   `NEVER`: This keyword indicates that a specific condition or constraint should never be met in the generated content.
    
-   `WITH`: This keyword is used to specify that the generated content should include certain properties or attributes.
    
-   `AND`: This keyword is used to combine multiple conditions or constraints in the generated content.
    
-   `ONLY`: This keyword is used to indicate that the generated content should exclusively meet certain conditions or constraints.
    
-   `NOT`: This keyword is used to negate a condition or constraint, meaning that the specified property or attribute should not be present in the output.
    
-   `UNIQUE`: This keyword is used to indicate that the generated content should be original and not duplicate any existing content.

### Keyword functions

-   `BETWEEN({{key1}}, {{key2}})`: This syntax can be used to specify a range for a certain attribute or property, indicating that the generated content should have a value between `key1` and `key2`.

-   `RANDOM({{key1}}, {{key2}}, ...)`: This syntax can be used to specify that the generated content should include one of the provided keys at random.

-   `MIXED({{key1}}, {{key2}}, ...)`: This syntax can be used to specify that the generated content should include a combination of the provided keys.

-   `CONTAINS({{key}})`: This syntax can be used to indicate that the generated content must contain the specified key.

-   `OPTIMIZE({{key}})`: This syntax can be used to suggest that the generated content should optimize for a certain aspect, such as readability or keyword density, represented by the key.

-   `LIMIT({{key}}, {{value}})`: This syntax can be used to set a limit on the number of times the specified key can appear in the generated content.

    
## functions

-   `fn(-{{key}})`: This syntax represents a function `fn` that takes the value of `key` as an input and removes or subtracts it from the generated content.
    
-   `fn(*{{key}})`: This syntax represents a function `fn` that takes the value of `key` as an input and repeats a specific property or attribute `key` times.
    
-   `fn(?{{key1}}:{{key2}})`: This syntax represents a function `fn` that takes the values of `key1` and `key2` as inputs and includes `key2` in the generated content if the condition specified by `key1` is met.
            
-   `fn(+{{key}})`: This syntax represents a function `fn` that takes the value of `key` as an input and appends or concatenates it with another element.
    
-   `fn(~{{key}})`: This syntax represents a function `fn` that takes the value of `key` as an input and generates content with a length close to the value of `key`.
        
-   `fn(BETWEEN({{key1}}, {{key2}}))`: This syntax represents a function `fn` that takes the values of `key1` and `key2` as inputs and generates content with a value between `key1` and `key2`

-   `fn(RANDOM({{key1}}, {{key2}}, ...))`: This syntax represents a function `fn` that takes multiple keys as inputs and generates content with one of the provided keys at random.

-   `fn(MIXED({{key1}}, {{key2}}, ...))`: This syntax represents a function `fn` that takes multiple keys as inputs and generates content with a combination of the provided keys.   
    
-   `fn(CONTAINS({{key}}))`: This syntax represents a function `fn` that takes the value of `key` as an input and ensures the generated content contains the specified key.
    
-   `fn(OPTIMIZE({{key}}))`: This syntax represents a function `fn` that takes the value of `key` as an input and generates content optimized for the specified aspect.
        
-   `fn(LIMIT({{key}}, {{value}}))`: This syntax represents a function `fn` that takes the values of `key` and `value` as inputs and generates content with a limit on the number of times the specified key can appear.

## Typing values

-   `"boolean"`: A value of the boolean data type, which can be either `true` or `false`.
    
-   `"string"`: A value of the string data type, which can consist of any combination of characters.
    
-   `"number"`: A value of the number data type, which can be any numerical value, including integers and floating-point numbers.

-   `"int"`: A value of the integer data type, which can be any whole number, including positive, negative, and zero values.

-   `"float"`: A value of the floating-point data type, which can be any real number, including integers, decimal values, and values in scientific notation.

-   `"one word"`: A value that should be a single word.
    
-   `"concise string"`: A value that should be a short and clear string.
    
-   `"detailed string"`: A value that should be a more detailed and descriptive string.
    
-   `"very detailed string"`: A value that should be even more detailed and comprehensive.
    
-   `"very detailed elaborative string"`: A value that should be extremely detailed and provide an elaborate explanation.
    
-   `"1-5"`: A value that should be within the range of 1 to 5, inclusive.
    
-   `10`: An exact value of 10.
    
-   `["string"]`: An array containing a single string element.

-   `"string[] *~10"`: An array of strings with an approximate length of 10 elements.
    
-   `"string[] *3"`: An array of strings with an exact length of 3 elements.
    
-   `"string[] *>=2"`: An array of strings with a length greater than or equal to 2 elements.
    
-   `"markdown<code:typescript>"`: A value that should be a Markdown-formatted string containing TypeScript code.
    
-   `"markdown<code:json>"`: Avalue that should be a Markdown-formatted string containing JSON code.
    
-   `"format<json>"`: A value that should be formatted as a JSON string.
