---
title: Suggest a Topic Form
sidebar: mydoc_sidebar
permalink: mydoc_suggest.html
folder: mydoc
---

To suggest a **new topic** or **sub-topic for an existing topic**, please read the [content quality guidelines](mydoc_guides.html#content-quality-guidelines) and complete the contact form following the template below:

**Template for new topic**:

```
New topic name:
Potential sub-topics:
Brief summary of the topic: 
Why this topic is important in the context of this website:
```

**Template for new subtopic for existing topic**:

```
Name of the existing section:
New sub-topic name:
Brief summary of the sub-topic: 
Why this sub-topic is important in the context of this website:
```

<style>
input[type="text"], input[type="email"], input[type="search"], 
input[type="submit"], button, textarea { 
  padding: 1em 1.5em; 
  border: 1px solid #e5e5e5; 
  border-radius: 30px; 
  margin-bottom: 1em; 
  font-family:  -apple-system, BlinkMacSystemFont, "Segoe UI", 
                "Roboto", "Oxygen", "Ubuntu", "Cantarell", 
                "Fira Sans", "Droid Sans", "Helvetica Neue", 
                Arial, sans-serif; 
}

textarea { width: 100%;  resize: none; }
</style>

<form id="fs-frm" name="simple-contact-form" accept-charset="utf-8" action="https://formspree.io/xbjzqgzo" method="post">
  <fieldset id="fs-frm-inputs">
    <label for="full-name">Full Name</label>
    <input type="text" name="name" id="full-name" placeholder="First and Last" required="">
    <label for="email-address">Email Address</label>
    <input type="email" name="_replyto" id="email-address" placeholder="youremail@domain.com" required="">
    <br>
    <label for="message">Message</label>
    <br>
    <textarea rows="6" name="message" id="message" placeholder="Please use the template above to suggest your topic" required=""></textarea>
    <input type="hidden" name="_subject" id="email-subject" value="Contact Form Submission">
  </fieldset>
  <input type="submit" value="Submit">
</form>

{% include links.html %}
