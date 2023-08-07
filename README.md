# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
*


質問内容：
ログアウト⇒ログインすると
NoMethodError in PostImages#indexエラー

Showing /home/ec2-user/environment/meshiterro/app/views/post_images/index.html.erb where line #4 raised:

undefined method `get_image' for nil:NilClass
Extracted source (around line #4):


  <div>
    <%= link_to post_image_path(post_image.id) do %>
      <%= image_tag @post_image.get_image %>☚
    <% end %>
    <p>投稿ユーザー画像：<%= image_tag post_image.user.get_profile_image(100,100) %></p>
    <p>ショップ名：<%= post_image.shop_name %></p>
