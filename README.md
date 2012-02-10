# paperclip-smusher

JPEG and PNG compression processor for Paperclip.

## Requirements

paperclip-smusher requires Paperclip gem, [jpegtran](http://jpegclub.org) and [optipng](http://optipng.sourceforge.net/) libraries.

## Installation

Add to your Gemfile

````ruby
gem "paperclip-smusher", "~> 0.1.0"
````

## Usage

````ruby
class User < ActiveRecord::Base
  has_attached_file :avatar,
                    :styles     => { :medium => "300x300>", :thumb => "100x100>" },
                    :processors => [:thumbnail, :compression]
end
````
