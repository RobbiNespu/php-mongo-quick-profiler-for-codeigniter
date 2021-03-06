###Update : Added codes to profile MongoDB. 
You can profile not only mySQL queries but also quries from MongoDB as well in this profiler. 
To activate MongoDB profilling just use my [MongoDB library for Codeigniter](https://github.com/intekhabrizvi/Codeigniter-mongo-library)

###Snapshot
![Image of profiller](http://intekhabrizvi.github.io/profiller.png)

So the amazing guys at Particletree built this awesome php profiler and I 
thought I would share my mods of integrating it into CI.  My code is a bit of a
hack job but you should get the idea.  Start by checking out the 
Particletree blog post at [http://particletree.com/features/php-quick-profiler/](http://particletree.com/features/php-quick-profiler/).
Reading through that will give you an idea of what the profiler can accomplish 
and how to log to its console.

The original, [danmorin](https://github.com/danmorin/php-quick-profiler-for-codeigniter) and [my codes](https://github.com/intekhabrizvi/php-mongo-quick-profiler-for-codeigniter) are released under Creative Commons Attribution 
3.0 License.

### Install

1. Make sure that hooks are enabled in your `application/config/config.php` file.

2. Copy the files from the download to the corresponding directories in your  
   application directory. Make sure you don't overwrite any of your own files  
   if you've customized them. You may need to create the plugins directory  
   under application.  
   > config      => system/application/config  
   > libraries   => system/application/libraries  
   > plugins     => system/application/plugins

3. Once that's done, anywhere you enable the profiler using  
   `$this->output->enable_profiler(TRUE)`, you should see the new profiler

### Notes

- The plugin is loading using hooks so it can be initialized before most of the  
  CI system. You could autoload it instead, but you'd miss out on a lot of  
  the CI loading process.

- It's not php4 compatible. If you use php4 still, think of this as a  
  fantastic perk you get once you finally upgrade. Oh and upgrade from  
  IE6 while you're at it too please ;)

### Bugs

- Images don't currently work correctly
