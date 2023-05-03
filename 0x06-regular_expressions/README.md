# 0x06. Regular expression

RegexDevOps

- By: Sylvain Kalache
- Weight: 1
- Project will start May 3, 2023 6:00 AM, must end by May 4, 2023 6:00 AM
- Checker was released at May 3, 2023 12:00 PM
- An auto review will be launched at the deadline

### Concepts

_For this project, we expect you to look at this concept:_

- [Regular Expression](https://intranet.alxswe.com/concepts/29)

## Background Context

For this project, you have to build your regular expression using Oniguruma, a regular expression library that which is used by Ruby by default. Note that other regular expression libraries sometimes have different properties.

Because the focus of this exercise is to play with regular expressions (regex), here is the Ruby code that you should use, just replace the regexp part, meaning the code in between the `//`:

```
sylvain@ubuntu$ cat example.rb
#!/usr/bin/env ruby
puts ARGV[0].scan(/127.0.0.[0-9]/).join
sylvain@ubuntu$
sylvain@ubuntu$ ./example.rb 127.0.0.2
127.0.0.2
sylvain@ubuntu$ ./example.rb 127.0.0.1
127.0.0.1
sylvain@ubuntu$ ./example.rb 127.0.0.a
```

## Resources

**Read or watch**:

- [Regular expressions - basics](https://intranet.alxswe.com/rltoken/6VeaVMaugIxcFAwA27TBdQ "Regular expressions - basics")
- [Regular expressions - advanced](https://intranet.alxswe.com/rltoken/rntjh3-3S86zt0Qy28L10w "Regular expressions - advanced")
- [Rubular is your best friend](https://intranet.alxswe.com/rltoken/RGkVuw1lZ_hoCCbLsiOAhg "Rubular is your best friend")
- [Use a regular expression against a problem: now you have 2 problems](https://intranet.alxswe.com/rltoken/Vwm8lpMUGa4x_FBtlyUQ8g "Use a regular expression against a problem: now you have 2 problems")
- [Learn Regular Expressions with simple, interactive exercises](https://intranet.alxswe.com/rltoken/XsQ6rzS1uy-E6bnswUqIKg "Learn Regular Expressions with simple, interactive exercises")

## Requirements

### General

- Allowed editors: `vi`, `vim`, `emacs`
- All your files will be interpreted on Ubuntu 20.04 LTS
- All your files should end with a new line
- A `README.md` file, at the root of the folder of the project, is mandatory
- All your Bash script files must be executable
- The first line of all your Bash scripts should be exactly `#!/usr/bin/env ruby`
- All your regex must be built for the Oniguruma library

### Quiz questions

**Great!** You've completed the quiz successfully! Keep going! (Hide quiz)

#### Question #0

What is the `/Scho.l/` regexp matching?

- [x] 
    
    School
    
- [ ] 
    
    school
    
- [x] 
    
    Scho.l
    

#### Question #1

What is the `/Scho*l/` regexp matching?

- Scho.l
    
- Schoo.l
    
- Schoool
    

#### Question #2

What is the `/school/` regexp matching?

- School
    
- school
    
- schoOl
    

## Tasks

### 0\. Simply matching School

mandatory

![](https://s3.amazonaws.com/alx-intranet.hbtn.io/uploads/medias/2020/9/ec65557f0da1fbfbff6659413885e4d4822f5b1d.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIARDDGGGOUSBVO6H7D%2F20230503%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20230503T134823Z&X-Amz-Expires=86400&X-Amz-SignedHeaders=host&X-Amz-Signature=10c226c4c5a3d82c5953b5e56b8503494c563ec269d05995ae6a600a4edd19ae)

Requirements:

- The regular expression must match `School`
- Using the project instructions, create a Ruby script that accepts one argument and pass it to a regular expression matching method

Example:

```
sylvain@ubuntu$ ./0-simply_match_school.rb School | cat -e
School$
sylvain@ubuntu$ ./0-simply_match_school.rb "Best School" | cat -e
School$
sylvain@ubuntu$ ./0-simply_match_school.rb "School Best School" | cat -e
SchoolSchool$
sylvain@ubuntu$ ./0-simply_match_school.rb "Grace Hopper" | cat -e
$
```

**Repo:**

- GitHub repository: `alx-system_engineering-devops`
- Directory: `0x06-regular_expressions`
- File: `0-simply_match_school.rb`

Done?! Help Check your code Get a sandbox

### 1\. Repetition Token #0

mandatory

![](https://s3.amazonaws.com/alx-intranet.hbtn.io/uploads/medias/2020/9/e7db3c377d46453588fc84f3a975661d142fee91.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIARDDGGGOUSBVO6H7D%2F20230503%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20230503T134823Z&X-Amz-Expires=86400&X-Amz-SignedHeaders=host&X-Amz-Signature=b33dca31136881f689d57568195c87aaf0740edd08bff88089051f91fb4bde7b)

Requirements:

- Find the regular expression that will match the above cases
- Using the project instructions, create a Ruby script that accepts one argument and pass it to a regular expression matching method

**Repo:**

- GitHub repository: `alx-system_engineering-devops`
- Directory: `0x06-regular_expressions`
- File: `1-repetition_token_0.rb`

Done?! Help Check your code Get a sandbox

### 2\. Repetition Token #1

mandatory

![](https://s3.amazonaws.com/alx-intranet.hbtn.io/uploads/medias/2020/9/c59ff11db195d5cf17d1790a5141ae2f234786d2.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIARDDGGGOUSBVO6H7D%2F20230503%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20230503T134823Z&X-Amz-Expires=86400&X-Amz-SignedHeaders=host&X-Amz-Signature=74767bbe45cb90f8acd6cd11cb52257ab0c0189abda085faadcc012259a87c2a)

Requirements:

- Find the regular expression that will match the above cases
- Using the project instructions, create a Ruby script that accepts one argument and pass it to a regular expression matching method

**Repo:**

- GitHub repository: `alx-system_engineering-devops`
- Directory: `0x06-regular_expressions`
- File: `2-repetition_token_1.rb`

Done?! Help Check your code Get a sandbox

### 3\. Repetition Token #2

mandatory

![](https://s3.amazonaws.com/alx-intranet.hbtn.io/uploads/medias/2020/9/3b6bf4aeca6a0c2de584e7f5d68d11eef57ce205.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIARDDGGGOUSBVO6H7D%2F20230503%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20230503T134823Z&X-Amz-Expires=86400&X-Amz-SignedHeaders=host&X-Amz-Signature=78de4f76bfc81ec1651c52b9c6b45d9eb19d21dbd3c2c92377c8265ece45786d)

Requirements:

- Find the regular expression that will match the above cases
- Using the project instructions, create a Ruby script that accepts one argument and pass it to a regular expression matching method

**Repo:**

- GitHub repository: `alx-system_engineering-devops`
- Directory: `0x06-regular_expressions`
- File: `3-repetition_token_2.rb`

Done?! Help Check your code Get a sandbox

### 4\. Repetition Token #3

mandatory

![](https://s3.amazonaws.com/alx-intranet.hbtn.io/uploads/medias/2020/9/f8dbcb9cf5ae569a8645027dc46e81cb372ce28e.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIARDDGGGOUSBVO6H7D%2F20230503%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20230503T134823Z&X-Amz-Expires=86400&X-Amz-SignedHeaders=host&X-Amz-Signature=b3a3a600001e84f6f645ac100abe63d3f15d87b54ac41eaf3bb22c8caf955a93)

Requirements:

- Find the regular expression that will match the above cases
- Using the project instructions, create a Ruby script that accepts one argument and pass it to a regular expression matching method
- Your regex should not contain square brackets

**Repo:**

- GitHub repository: `alx-system_engineering-devops`
- Directory: `0x06-regular_expressions`
- File: `4-repetition_token_3.rb`

Done?! Help Check your code Get a sandbox

### 5\. Not quite HBTN yet

mandatory

Requirements:

- The regular expression must be exactly matching a string that starts with `h` ends with `n` and can have any single character in between
- Using the project instructions, create a Ruby script that accepts one argument and pass it to a regular expression matching method

Example:

```
sylvain@ubuntu$ ./5-beginning_and_end.rb 'hn' | cat -e
$
sylvain@ubuntu$ ./5-beginning_and_end.rb 'hbn' | cat -e
hbn$
sylvain@ubuntu$ ./5-beginning_and_end.rb 'hbtn' | cat -e
$
sylvain@ubuntu$ ./5-beginning_and_end.rb 'h8n' | cat -e
h8n$
sylvain@ubuntu$
$
```

**Repo:**

- GitHub repository: `alx-system_engineering-devops`
- Directory: `0x06-regular_expressions`
- File: `5-beginning_and_end.rb`

Done?! Help Check your code Get a sandbox

### 6\. Call me maybe

mandatory

This task is brought to you by a professional advisor [Neha Jain](https://intranet.alxswe.com/rltoken/GqwvXAvTXR_JXqyTvZ4AzQ "Neha Jain"), Senior Software Engineer at LinkedIn.

Requirement:

- The regular expression must match a 10 digit phone number

Example:

```
sylvain@ubuntu$ ./6-phone_number.rb 4155049898 | cat -e
4155049898$
sylvain@ubuntu$ ./6-phone_number.rb " 4155049898" | cat -e
$
sylvain@ubuntu$ ./6-phone_number.rb "415 504 9898" | cat -e
$
sylvain@ubuntu$ ./6-phone_number.rb "415-504-9898" | cat -e
$
sylvain@ubuntu$
```

**Repo:**

- GitHub repository: `alx-system_engineering-devops`
- Directory: `0x06-regular_expressions`
- File: `6-phone_number.rb`

Done?! Help Check your code Get a sandbox

### 7\. OMG WHY ARE YOU SHOUTING?

mandatory

![](/images/contents/sysadmin/projects/78/shouting.jpg)

Requirement:

- The regular expression must be only matching: capital letters

Example:

```
sylvain@ubuntu$ ./7-OMG_WHY_ARE_YOU_SHOUTING.rb "I realLy hOpe VancouvEr posseSs Yummy Soft vAnilla Dupper Mint Ice Nutella cream" | cat -e
ILOVESYSADMIN$
sylvain@ubuntu$ ./7-OMG_WHY_ARE_YOU_SHOUTING.rb "WHAT do you SAY?" | cat -e
WHATSAY$
sylvain@ubuntu$ ./7-OMG_WHY_ARE_YOU_SHOUTING.rb "cannot read you" | cat -e
$
sylvain@ubuntu$
```

**Repo:**

- GitHub repository: `alx-system_engineering-devops`
- Directory: `0x06-regular_expressions`
- File: `7-OMG_WHY_ARE_YOU_SHOUTING.rb`
