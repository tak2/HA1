# HA1
A blueprint for hosting multiple wordpress sites in one VM

lets put the ground rules we will use cloudflare for SSL and monitoring and chaching

then Nginx for resvers proxy to use the same Docker on tthe VM and 



https://www.digitalocean.com/community/questions/how-to-host-multiple-docker-containers-on-a-single-droplet-with-nginx-reverse-proxy


move wordpress to diffrent place
https://wpbeaches.com/updating-wordpress-mysql-database-after-moving-to-a-new-url/

UPDATE wp_options SET option_value = replace(option_value, 'http://www.oldurl', 'http://www.newurl') WHERE option_name = 'home' OR option_name = 'siteurl';
UPDATE wp_posts SET guid = replace(guid, 'http://www.oldurl','http://www.newurl');
UPDATE wp_posts SET post_content = replace(post_content, 'http://www.oldurl', 'http://www.newurl');
UPDATE wp_postmeta SET meta_value = replace(meta_value,'http://www.oldurl','http://www.newurl');
