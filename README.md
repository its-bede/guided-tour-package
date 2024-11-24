# Guided Tour

A simple Stimulus controller that enables you to show a guided tour overlay on your website. It requires Bootstrap to be installed and have Popover loaded.

This package has a corresponding ruby gem. See [guided-tour](https://github.com/its-bede/guided_tour) repo.

## Installation

```bash
npm install @itsbede/guided-tour
```

## Usage

```javascript
// In your application
import GuidedTourController from '@itsbede/guided-tour'
application.register('guided-tour', GuidedTourController)
```

```html
<!-- modify to your gusto -->
<div class="guided-tour--wrapper"
     data-controller="guided-tour--tour"
     data-guided-tour__tour-next-btn-text-value="Next"
     data-guided-tour__tour-prev-btn-text-value="Previous"
     data-guided-tour__tour-done-btn-text-value="Done"
     data-guided-tour__tour-step-line-text-value="Step">

  <div class="guided-tour--starter-btn-wrapper">
    <button type="button" class="btn btn-primary ms-auto" id="guidedTourStarterBtn">
      <i class="bi bi-lightbulb"></i>
      &nbsp;
      Start Tour
    </button>
  </div>

  <div class="guided-tour--overlay"
       data-guided-tour__tour-target="overlay"
       data-bs-container="body"
       data-bs-toggle="popover"
       data-bs-placement="bottom"
       data-bs-content="">
  </div>

  <ol class="d-none">
    <li data-guided-tour__tour-target="explanation"
        data-target-element="step1">
      This is the first step of the tour
    </li>
    <li data-guided-tour__tour-target="explanation"
        data-target-element="step2">
      This is the second step of the tour
    </li>
    <li data-guided-tour__tour-target="explanation"
        data-target-element="step3">
      This is the final step of the tour
    </li>
  </ol>
</div>
```