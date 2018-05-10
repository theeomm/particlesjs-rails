# particlesjs-rails

particlesjs-rails is a ruby on rails wrapper for [particle.js](https://github.com/VincentGarreau/particles.js)

Source: [https://github.com/VincentGarreau/particles.js](https://github.com/VincentGarreau/particles.js)

Ruby Gem: [https://rubygems.org/gems/particlesjs-rails](https://rubygems.org/gems/particlesjs-rails)

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'particlesjs-rails'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install particlesjs-rails

In `app/assets/javascripts/application.js` add:
```javascript
//= require particles
```

## Usage

* In your views, assign an `id` to the element were you want the particles to appear. In this case lets call it `particles`

* create a javascript file in `app/assets/javascripts/my-particles.js`. You can initialize particles.js as shown in example:

```javascript
document.addEventListener('turbolinks:load',() => {
    particlesJS('particles', {
        "particles": {
            "number": {
            "value": 80,
            "density": {
                "enable": true,
                "value_area": 800
            }
            },
            "color": {
            "value": "#ffffff"
            },
            "shape": {
            "type": "circle",
            "stroke": {
                "width": 0,
                "color": "#000000"
            },
            "polygon": {
                "nb_sides": 5
            },
            "image": {
                "src": "img/github.svg",
                "width": 100,
                "height": 100
            }
            },
            "opacity": {
            "value": 0.5,
            "random": false,
            "anim": {
                "enable": false,
                "speed": 1,
                "opacity_min": 0.1,
                "sync": false
            }
            },
            "size": {
            "value": 10,
            "random": true,
            "anim": {
                "enable": false,
                "speed": 80,
                "size_min": 0.1,
                "sync": false
            }
            },
            "line_linked": {
            "enable": true,
            "distance": 300,
            "color": "#ffffff",
            "opacity": 0.4,
            "width": 2
            },
            "move": {
            "enable": true,
            "speed": 12,
            "direction": "none",
            "random": false,
            "straight": false,
            "out_mode": "out",
            "bounce": false,
            "attract": {
                "enable": false,
                "rotateX": 600,
                "rotateY": 1200
            }
            }
        },
        "interactivity": {
            "detect_on": "canvas",
            "events": {
            "onhover": {
                "enable": false,
                "mode": "repulse"
            },
            "onclick": {
                "enable": true,
                "mode": "push"
            },
            "resize": true
            },
            "modes": {
            "grab": {
                "distance": 800,
                "line_linked": {
                "opacity": 1
                }
            },
            "bubble": {
                "distance": 800,
                "size": 80,
                "duration": 2,
                "opacity": 0.8,
                "speed": 3
            },
            "repulse": {
                "distance": 400,
                "duration": 0.4
            },
            "push": {
                "particles_nb": 4
            },
            "remove": {
                "particles_nb": 2
            }
            }
        },
        "retina_detect": true
        })
    })
```

## Contributing

Bug reports and pull requests are welcome. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

## License

The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).