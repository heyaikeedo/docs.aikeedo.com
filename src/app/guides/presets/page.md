---
title: Prompt Templating Documentation
nextjs:
  metadata:
    title: Prompt Templating Documentation
    description: Prompt templating is a feature that allows the creation of dynamic prompts with customizable inputs.
---

Prompt templating is a feature that allows the creation of dynamic prompts with customizable inputs. These prompts are constructed using simple text templates containing tags and attributes that are replaced with actual values during prompt generation. {% .lead %}

## Tags and Attributes

### Tags

Tags are placeholders within curly braces, such as `{ input_name }`. They represent input elements that users can customize.

### Attributes

Attributes are methods that modify the behavior of tags. They are appended to tags using the pipe character (`|`). Multiple attributes can be applied to a single tag.

## Syntax

The default syntax renders each input as a simple text input with a label:

```plaintext
{ input_name }
```

The label is automatically generated from the input name in title case. This behavior can be overridden using the `label` attribute:

```plaintext
{ input_name | label:Blog title }
```

Multiline text inputs are defined using the `multiline` attribute:

```plaintext
{ input_name | multiline }
```

A custom label for multiline inputs can be set as follows:

```plaintext
{ input_name | multiline | label:Input name }
```

An input with predefined options is defined using the `type` attribute with a value of `enum`. The options are defined using the `options` attribute:

```plaintext
{ input_name | type:enum | options:Option 1, Option 2, Option 3 }
```

## Available Attributes

### label

The `label` attribute is used to set a custom label for the input:

```html
{ input_name | label:Custom label }
```

### multiline

The `multiline` attribute defines a multiline text input:

```html
{ input_name | multiline }
```

### type

The `type` attribute defines the type of input. Currently the only possible value is `enum`.

```html
{ input_name | type:enum }
```

### options

The `options` attribute defines the options for an input with the `enum` type:

```html
{ input_name | type:enum | options:Option 1, Option 2, Option 3 }
```

### optional

The `optional` attribute makes an input optional:

```html
{ input_name | optional }
```

### placeholder

The `placeholder` attribute sets a custom placeholder for the input:

```html
{ input_name | placeholder:Custom placeholder }
```

### info

The `info` attribute provides custom information text for the input:

```html
{ input_name | info:Custom info text }
```

## Built-in Inputs

Currently, there are two built-in inputs:

- `language` - Dropdown list of supported languages.
- `tone` - Dropdown list of supported voice tones.

Built-in inputs are simple tags with no attributes:

```plaintext
{ language }
```

```plaintext
{ tone }
```

## Creating Prompt Templates

To create a prompt template for an "Article Generator," use the following example:

```plaintext

    Write an article about { topic | placeholder: Your chosen subject | info:
    Important details }. Use the following draft content:

    ---
        { content | multiline| placeholder: Draft content }
    ---

    Additional instructions:
    - Include relevant statistics (add the links of the sources you use)
    and consider diverse perspectives.
    - Write it in a { language } language by using {tone} voice tone and
    mention the source links in the end.

```

This template generates a form for users to input the topic, draft content, language, and tone for an article.

If you have any questions or need assistance, feel free to [reach out to our support team](mailto:support@aikeedo.com).
