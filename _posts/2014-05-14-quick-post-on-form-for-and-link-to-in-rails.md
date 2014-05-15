---
layout: post
title: form_for and link_to
---


###form_for and link_to

####link_to

- `link_to` generates the html for a link. It takes several parameters:
	- :name - a string
	- :url - here you can pass a string or, more likely, your route name, like `object_path(@object)`
	- `:data` hash
	- Method: symbol of HTTP verb
		- defaults to `:get`
		- can be `:post`, `:delete`, `:patch`, and `:put`.
	- Example syntax:
	`<%= link_to("Delete", object_path(@object), :method => delete%>)`

####form_for

- `form_for` generates HTML to take in info to create or update a model object. It takes some parameters:

	- Also takes another argument: a hash of options that include `:url`, `:namespace`, `:html`. Here's an example:
	`<%= form_for @object, url: {action: "update"} do |f| %>
  		First name: <%= f.text_field :first_name %><br />
  	  <%= f.submit %>
	<% end %>`

	- `form_tag` is a way to append fields that have nothing to do with the subject of the rest of the form.



