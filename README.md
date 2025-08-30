# A flexible array in C language

A shared library which provides a set of functions for handling a flexible array in C.

<h2>How to download?</h2>
You can download it <a href="https://github.com/user-attachments/files/22059006/libArray.zip">here</a>

<h2>How to install?</h2>
Unzip the downloaded file and move libArray.so to /usr/lib

<h2>How to link?</h2>
You can link the library to your C project as follows: gcc example.c -l Array

<br>
<h2> Examples </h2>

* Example A:

<pre>
<code class="language-c">
#include &lt;stdio.h&gt;
#include &lt;stdlib.h&gt;
#include "Array.h"

int main()
{
    Array* matrix = Array_init ([
        [1, 2, 3],
        [4, 5, 6],
        [7, 8, 9]
    ]);

    printf("Array matrix: ");
    Array_println(matrix);

    Array_delete(matrix);
    
    return EXIT_SUCCESS;
}
</code>
</pre>

output:
<pre> Array matrix: [[1, 2, 3], [4, 5, 6], [7, 8, 9]] </pre>

* Example B:

<pre>
<code class="language-c">
#include &lt;stdio.h&gt;
#include &lt;stdlib.h&gt;
#include "Array.h"

int main()
{
    Array* data = Array_object();
    
    Array_append(data, "Hello world");
    Array_append(data, "Z");
    Array_append(data, 123);
    Array_append(data, 0.123);
    
    printf("Array data: ");
    Array_println(data);

    Array_delete(data);
    
    return EXIT_SUCCESS;
}
</code>
</pre>

output:
<pre> Array data: ['Hello world', 'Z', 123, 0.123] </pre>
