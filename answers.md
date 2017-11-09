1. Select the element that contains the profile image (hint: look for the class). Change the src attribute so it points to a picture of your choosing instead.

  var profileImage = document.querySelector('.profile-image')
  profileImage.src = 'https://placebear.com/g/400/400'

1. Use the same approach to select the element that contains the photo of the sky and change the src attribute to another picture URL of your choosing.

  var leftImage = document.querySelector('#left-image img')
  leftImage.src = 'https://picsum.photos/325/225'

2. Select the heading that says "Panda the Bear" and change it to your own name.

  var headText = document.querySelector('h1.highlight')
  headText.innerText = "Martin Maco"

3. Select the heading that says "Employment" and change it to something else. (hint: use a descendant selector)

  var employmentText = document.querySelector('#employment .info-title')
  employmentText.innerHTML = '<i class="icon-suitcase"></i> &nbsp; Pass Work'

4. Change the colour of the body.

  var background = document.querySelector('body')
  background.style.backgroundColor = "lightblue"

5. Change the colour of each element using the highlight class. Use a for loop to do this.

  var highlightClassed = document.querySelectorAll('.highlight')
  highlightClassed.forEach(function(element){ element.style.backgroundColor = 'orange' })

6. Change the font family of the h1 to 'monospace'.

  var docH1 = document.querySelector('h1')
  docH1.style.fontFamily = 'monospace'

7. Find a way to select the round icons in the sidebar and then change their colour.

  var actionIconsBck = document.querySelectorAll('a.action-icon-bg')
  actionIconsBck.forEach(function(icon){ icon.style.backgroundColor = 'blue' })

8. Scroll down to the contact form. Change the placeholder attribute of the name field to "identify yourself".

  var inputName = document.querySelector('input[name="name"')
  inputName.placeholder = 'Identify yourself'

9. Change the placeholder attribute of the message field to "state your business".

  var inputMessage = document.querySelector('textarea')
  inputMessage.placeholder = 'State your business'

10. Give the name field a "value" attribute of "your nemesis".

  var nameInputValue = document.querySelector('input[name="name"]')
  nameInputValue.setAttribute('value', 'your nemesis')

11. Change the value attribute of the email field to "koalathebear@gmail.com".

  var emailInputValue = document.querySelector('input[type="email"]')
  emailInputValue.setAttribute('value', 'koalathebear@gmail.com')

12. Change the value of the submit button on the contact form to "En garde!".

  var inputSubmit = document.querySelector('input[type="submit"]')
  inputSubmit.setAttribute('value', "En garde!")

13. We should stop Koala from sending an email to Panda that they might regret! Find a way to disable the submit button (hint: familiarize yourself with the disabled attribute).

    var inputSubmit = document.querySelector('input[type="submit"]')
    inputSubmit.setAttribute("disabled", "disabled")

14. We should help Panda protect their privacy by erasing their personal details from the sidebar.

  var pandaBio = document.querySelector('ul.bio-info')
  pandaBio.remove()
