# reading notes 


mobile phones are so popular these days that designing a web site effeciently require that you make it for the phone first and the full scale version is set to trigger when the "break point" is reached so basically you have to math matically set up your css to be flexable to be both on a phone and a tablet and desktop

so in come the css float tricks so obviously there is tons of information in here bookmarked to refer back to later and also 

math equation for break point

*target ÷ context = result

What are floats used for?
Aside from the simple example of wrapping text around images, floats can be used to create entire web layouts.

#footer {
  clear: value of your choice;			
}

clear has 4 valid values as well 
both 
left
right
none

Inherit would be the fifth, but is strangely not supported in Internet Explorer.


Identifying Breakpoints
Your instinct might be to write media query breakpoints around common viewport sizes as determined by different device resolutions, such as 320px, 480px, 768px, 1024px, 1224px, and so forth. This is a bad idea.

When building a responsive website it should adjust to an array of different viewport sizes, regardless of the device. Breakpoints should only be introduced when a website starts to break, look weird, or the experience is being hampered.

Additionally, new devices and resolutions are being released all of the time. Trying to keep up with these changes could be an endless process.

Flexible Media
The final, equally important aspect to responsive web design involves flexible media. As viewports begin to change size media doesn’t always follow suit. Images, videos, and other media types need to be scalable, changing their size as the size of the viewport changes.

One quick way to make media scalable is by using the max-width property with a value of 100%. Doing so ensures that as the viewport gets smaller any media will scale down according to its containers width.