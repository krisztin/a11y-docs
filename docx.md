# How to create accessible documents

[Based on 508 guidelines](https://www.section508.gov/create/documents/)

In short, use built in features and don't do manual formatting.

**Word inbuilt accessibility checker**

It's only good to check certain issues (images, alignment)

`File > Info > Check for issues > Check for accessibility`

## Accessible document checklist

1. **Save as .docx with a descriptive filename**

2. **Use styles to create headings**

3. **Use built-in list feature for lists**

4. **Use built-in organisation features**

   i.e. columns instead of tabs or spaces

5. **Tables**

   Can do simple data tables with a single header cell row but if you add another header line e.g first row is days of week, top row would be weekdays / weekend, then it no longer works. Merged or split cells make a table complex and hence inaccessible

   table is accessible if:

   - reading order is correct (`Tab` through it to see)
   - on table tab text wrapping is set to none `RCL > table properties`
   - if header then `table tools > repeat header row`

   check a11y:

   - check for merged split cells by toggling `grid lines`
   - header row: click in header row `shft+f1` (reveal formatting) ROW should be `repeat as header row`

6. ID languages

   Use `Set Proofing Language` to appropriate language

   `review > language > set proofing language`

7. Create unambiguous names for links

8. Headers, footers watermarks

   Screen readers don't automatically read headers, footers, watermarks.

   If there's vital information in any of these, it needs to be duplicated within the document at or near the start

9. Accessible images and objects

   - use alt text, captions or text nearby appropriately
   - if decorative add a space or " "

10. Textboxes

    Need to be in line with text
    page layout > position > in line with text

11. Use colour and other sensory charactheristics PLUS text to convey meaning

    Do not use color, size etc. only to convey meaning, always include text that duplicates meaning

12. Appropriate contrast levels

13. Accessible embedded files

    If meaningful information.
    Audio-only - include an accurate and complete transcript in the Word document
    Video-only - accurate and complete text description of what's shown
    Multimedi - accurate and complete syncronised captions and audio description
