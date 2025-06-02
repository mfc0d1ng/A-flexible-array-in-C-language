# A dynamic array in C language

A shared library which provides a set of functions for handling a dynamic array in C.

<h2>How to download?</h2>
You can download it <a href="https://github.com/user-attachments/files/20559598/libArray.zip">here</a>

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
    Array* values = Array_construct ([[1, 2, 3], [4, 5, 6], [7, 8, 9]]);

    printf("Array values: ");
    Array_println(values);

    Array_delete(values);
    
    return EXIT_SUCCESS;
}
</code>
</pre>

output:
<pre> Array values: [[1, 2, 3], [4, 5, 6], [7, 8, 9]] </pre>

* Example B:

<pre>
<code class="language-c">
#include &lt;stdio.h&gt;
#include &lt;stdlib.h&gt;
#include "Array.h"

int main()
{
    Array* data = Array_object();
    
    Array_push(data, "Hello world");
    Array_push(data, (char)'Z');
    Array_push(data, 123);
    Array_push(data, 0.123);
    
    printf("ArrayList data: ");
    Array_println(data);

    Array_delete(data);
    
    return EXIT_SUCCESS;
}
</code>
</pre>

output:
<pre> Array data: ['Hello world', 'Z', 123, 0.123] </pre>
