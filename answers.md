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


PART2
REMOVING eLEMENTS FROM DOM

1. Panda the Bear is lying about their skills! Take the "time travel" skill off the page to satisfy your personal sense of justice.

  var timeTravel = $('div#time-travel').parent('.bar-default')  
  timeTravel.css("display", "none")

ADDING ELEMENTS TO THE DOM

1. That drawing of Pikachu is really cute. Let’s duplicate it using cloneNode() and insert it at the bottom of the .portfolio-container using insertAdjacentHTML() or appendChild().

  var pikachu = document.querySelector('img[title="Pikachu"]')
  var porfolioContainer = document.querySelector('div.portfolio-container')
  porfolioContainer.appendChild(pikachu2)

2. Wow, that was so satisfying I think we should do it 10 more times. Use a for loop to help you do this.

  for ( step = 0; step < 9; step ++ ){
    pikachuX = pikachu.cloneNode();
    porfolioContainer.appendChild(pikachuX)
  }

3. Let’s add a message about when the page was last updated. We'll do this by appending a new <li> element to the <ul> in the sidebar (you might need to refresh the page to bring back the list items that we emptied out earlier).

  var li = document.querySelector('li.bio-info-item')
  var ul = document.querySelector('ul.bio-info')
  var cloneLi = li.cloneNode(true)
  ul.appendChild(cloneLi)

  var infoTitle = document.querySelector('ul.bio-info li:last-child .bio-info-title')
  infoTitle.innerText = "Page Last updated on"

  var infoValue = document.querySelector('ul.bio-info li:last-child .bio-info-name')
  infoValue.innerText = new Date();

  other:::::::::::::

  var listItem = document.createElement('li');
    var leftSpan = document.createElement('span');
      var lastUpdated = document.createTextNode('Page last updated on');
    leftSpan.appendChild(lastUpdated);
  listItem.appendChild(leftSpan);
    var rightSpan = document.createElement('span')
      var dateUpdated = document.createTextNode(Date())
    rightSpan.appendChild(dateUpdated)
  listItem.appendChild(rightSpan);

  document.querySelector('.bio-info').appendChild(listItem);

  listItem.setAttribute("class","bio-info-item");

  listItem.setAttribute("class","bio-info-item");
    leftSpan.setAttribute("class", "bio-info-title");
    rightSpan.setAttribute("class", "bio-info-value");
