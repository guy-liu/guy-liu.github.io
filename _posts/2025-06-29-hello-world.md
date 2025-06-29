---
title: Hello World - But which world?
date: 2025-06-29 23:00:00
categories: [Programming, PowerShell]
tags:  [PowerShell, C#, Win32 API]
---
You probably already know that "Hello World!" tends to be the first program people write as one embarks on the journey to learn a new programming language. I indeed have found this unspoken rule to hold true over the many years I have worked with computers. In fact, I have found myself writting more "Hello World!" programs in recent years, as I had the opportunity (and need) to learn new programming languages. 

So this seems like a fitting place to start writting a new blog. 

To begin with, let's write a Hello World program in PowerShell, as I found it to be one of the most useful languages around.

``` powershell
"Hello World!"
```

That was meant to be a joke. But looking at it, I must admit there is beauty in simplicity. But let's stop goofing around and try something else.

I found Microsoft to be rather good at making their products work together with each other. So in Powershell, you can actually write native C# .NET code. When I heard about this many years ago, I found it unbelievable that you can write lines of a compiled language inside an interpreted language and it somehow just executes!

So let's try write a PowerShell Hello World program but actually use C# code instead.

But let's not stop there. Inside C#, you can actually write "unmanaged" code - code that are outside of the .NET platform and are written in other languages such as C++ and compiled into a DLL. This also means we can actually call functions from the Windows API (Win32 API) to perform the work we want to do - in this case, to print "Hello World!" to the console.

This starts to sound interesting, but it will take quite a bit of work to research all the materials and syntax and function parameters... So I asked AI to write this for me, and 30 seconds later...

``` powershell
Add-Type -TypeDefinition @"
using System;
using System.Runtime.InteropServices;

public class HelloWorld {
    [DllImport("kernel32.dll", SetLastError = true)]
    static extern IntPtr GetStdHandle(int nStdHandle);

    [DllImport("kernel32.dll", SetLastError = true)]
    static extern bool WriteConsole(IntPtr hConsoleOutput, string lpBuffer, uint nNumberOfCharsToWrite, out uint lpNumberOfCharsWritten, IntPtr lpReserved);

    const int STD_OUTPUT_HANDLE = -11;

    public static void SayHello() {
        IntPtr handle = GetStdHandle(STD_OUTPUT_HANDLE);
        string message = "Hello World!";
        uint charsWritten;
        WriteConsole(handle, message, (uint)message.Length, out charsWritten, IntPtr.Zero);
    }
}
"@

# Invoke the method
[HelloWorld]::SayHello()
```

As far as Hello World programs go, this is the polar opposite of simplicity. The example show cases the versatility of PowerShell and .NET languages, which I find very cool as a tech enthusiast. But as a cyber security practitioner, I naturally wonder about the implications this sort of capabilities have on the cyber threat landscape. 

The technology world now feels like a very different place compared to the time when I wrote my first Hello World program in BASIC many years ago. It is much more interconnected and therefore complex. But in some ways it also feels easier - I have just written a program (with the help of AI) that uses multiple programming language and some nifty trick features without really needing to know much about how to program in any of them.

What does this mean to people who are working in or wanting to get into this field? Do you need to know the fundamentals or is it best to just jump on the latest trend? Is newer always better? When does the old actually become obsolete? I hope to explore some of these themes in this blog.

In some ways, this is the first online blog entry I have ever written, so this is indeed a Hello World to tech blogging.

But in reality, I wrote this blog entry so I can have something to test the configuration of the comments section :-)