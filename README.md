# A dynamic array in C language

A shared library which provides a set of functions for handling a dynamic array in C.

<h2>How to download?</h2>
You can download it <a href="https://github.com/user-attachments/files/21815566/libarray.zip">here</a>

<h2>How to install?</h2>
Unzip the downloaded file and move libarray.so to /usr/lib

<h2>How to link?</h2>
You can link the library to your C project as follows: gcc example.c -l array

<br>
<h2> Examples </h2>

* Example A:

<pre>
<code class="language-c">
#include &lt;stdio.h&gt;
#include &lt;stdlib.h&gt;
#include "array.h"

int main()
{
    array* matrix = Array ([
        [1, 2, 3],
        [4, 5, 6],
        [7, 8, 9]
    ]);

    printf("array matrix: ");
    array_println(matrix);

    array_delete(matrix);
    
    return EXIT_SUCCESS;
}
</code>
</pre>

output:
<pre> array matrix: [[1, 2, 3], [4, 5, 6], [7, 8, 9]] </pre>

* Example B:

<pre>
<code class="language-c">
#include &lt;stdio.h&gt;
#include &lt;stdlib.h&gt;
#include "array.h"

int main()
{
    array* data = array_object();
    
    array_append(data, "Hello world");
    array_append(data, "Z");
    array_append(data, 123);
    array_append(data, 0.123);
    
    printf("array data: ");
    array_println(data);

    array_delete(data);
    
    return EXIT_SUCCESS;
}
</code>
</pre>

output:
<pre> array data: ['Hello world', 'Z', 123, 0.123] </pre>
