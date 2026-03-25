# Selectors-forms-exp4
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CSS Selectors Assignment</title>
    <style>
        /* i. SIMPLE SELECTORS */
        * { font-family: 'Segoe UI', Tahoma, sans-serif; } /* Universal selector */
        h1 { color: #2c3e50; }                             /* Element selector */
        #main-title { text-align: center; }                /* ID selector */
        .highlight { background-color: #f1c40f; }          /* Class selector */
        h2, h3 { border-bottom: 2px solid #3498db; }       /* Grouping selector */

        /* ii. COMBINATOR SELECTORS */
        article p { color: #7f8c8d; }                      /* Descendant selector (any p inside article) */
        div > p { font-weight: bold; }                     /* Child selector (direct p children of div) */
        h3 + p { font-style: italic; }                     /* Adjacent sibling (p immediately after h3) */
        h3 ~ p { text-decoration: underline; }             /* General sibling (all p after h3) */

        /* iii. PSEUDO-CLASS SELECTOR */
        button:hover { background-color: #2ecc71; color: white; cursor: pointer; }
        li:nth-child(odd) { color: #e67e22; }              /* Targets 1st, 3rd, etc. items */

        /* iv. PSEUDO-ELEMENT SELECTOR */
        p::first-letter { font-size: 200%; color: red; }   /* Styles the very first letter */
        .special-note::before { content: "⭐ ALERT: "; font-weight: bold; }

        /* v. ATTRIBUTE SELECTOR */
        input { border: 2px solid #3498db; padding: 5px; }
        a[target="_blank"] { color: #e74c3c; font-weight: bold; }
    </style>
</head>
<body>

    <h1 id="main-title">CSS Selector Forms</h1>

    <section>
        <h2>Simple & Grouping</h2>
        <p class="highlight">This paragraph uses a class selector.</p>
        <h3>Heading 3 (Grouped with H2)</h3>
    </section>

    <hr>

    <article>
        <h2>Combinators</h2>
        <div>
            <p>I am a direct child of a DIV (Bold).</p>
            <span>
                <p>I am a descendant of Article, but not a direct child of DIV.</p>
            </span>
        </div>
        <h3>An Adjacent Sibling Trigger</h3>
        <p>I am the adjacent sibling (Italic & Underlined).</p>
        <p>I am a general sibling (Underlined only).</p>
    </article>

    <hr>

    <section>
        <h2>Pseudo-Classes & Elements</h2>
        <ul>
            <li>Item 1 (Odd)</li>
            <li>Item 2 (Even)</li>
            <li>Item 3 (Odd)</li>
        </ul>
        <button>Hover Over Me!</button>
        <p class="special-note">This is a paragraph with a pseudo-element prefix.</p>
    </section>

    <hr>

    <section>
        <h2>Attribute Selectors</h2>
        <input type="text" placeholder="I have an attribute selector">
        <br><br>
        <a href="https://google.com" target="_blank">External Link (Red)</a> | 
        <a href="#">Internal Link (Default)</a>
    </section>

</body>
</html>
