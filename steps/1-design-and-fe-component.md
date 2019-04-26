# FE: Starting with a design and/or front-end component 

## Roles

* Primarily a FE developer to create the markup, styles and scripts required to create this component
* There would likely be collaboration and review with the UX team member who designed this component throughout this step

## CTA Assembly Mockup Example

Here is a reminder of what the mockup looked like in our last step.

![CTA Assembly Type Example](../img/cta-component.png "CTA Assembly Type Example")

## CTA Assembly Markup (Twig)

This is an example of what the CTA assembly markup (Twig) could be:

```twig
{#
/**
 * @file assembly.html.twig
 * Default theme implementation to present Assembly data.
 *
 * This template is used when viewing Assembly pages.
 *
 *
 * Available variables:
 * - content: A list of content items. Use 'content' to print all content, or
 * - attributes: HTML attributes for the container element.
 *
 * @see template_preprocess_assembly()
 *
 * @ingroup themeable
 */
#}
<section{{ attributes.addClass('assembly') }}{{ audience_selection }}>
  <div class="container">
  {% if content %}
    {{- content -}}
  {% endif %}
  </div>
  {% if background_image_url %}
    <div class="background" style="background-image: url({{ background_image_url }});"></div>
  {% endif %}
</section>
```

## CTA Assembly styles

This is an example of the styles of our CTA assembly type could be:

```scss
.assembly-type-call_to_action {
  background: $light-blue;
  color: #FFF;
  font-weight: bold;
  text-align: center;

  .text-formatted {
    color: #FFF;
    font-size: 18px;
    line-height: 1.5;
    @include tablet-portrait {
      font-size: 24px;
    }
  }

  .header {
    color: #FFF;
    font-size: 27px;
    line-height: 1.25;
    margin-bottom: 5px;
    @include tablet-portrait {
      font-size: 40px;
    }
    @include tablet-landscape {
      font-size: 57px;
      margin-bottom: 0;
    }
  }

  p, ul, ol {
    &:last-child {
      margin-bottom: 0;
    }
  }

  > .container > .button {
    &:last-child {
      margin-top: 24px;
      @include tablet-landscape {
        margin-top: 34px;
      }
    }
    &:first-child:last-child {
      margin-top: 0;
    }
  }

  &.left {
    float: none !important;
    text-align: left;
    .header {
      text-align: left;
    }
  }
  &.dark {
    background: #242424;
  }
}
```

### Deliverables

* The HTML markup (probably Twig) and assets (CSS, SCSS, JS, possibly images, etc.) required to satisfy the mockups.

[Previous page](./0-ux-mockup-and-data-structure.md)
[Next page](./2-creating-the-cta-assembly-type.md)
