---
layout: page
title: 台灣真菌多樣性
subtitle: 公民科學調查
permalink: "LoginPage"
#published: false
#<iframe src="https://ythuangmyco.github.io/fdcs_login/" height="700" width="100%" frameBorder="0"></iframe>
---
import React from 'react';
import ReactDom from 'react-dom';
import $ from "min-jquery";
import Header from './header';
import Footer from './footer';
//AJAX request
var GetStuff= React.createClass({
    getInitialState: function() {
      return {
        entries: []
      };
    },
    componentDidMount: function() {
        $.ajax({
          url: 'https://ythuangmyco.github.io/fdcs_login/',
          dataType: 'json',
          cache: false,
          success: function(data) {
            this.setState({entries: data});
            console.log('success');
          }.bind(this),
          error: function(xhr, status, err) {
            console.error(this.props.url, status, err.toString());
            console.log('fail');
          }.bind(this)
        });
      },
    render: function() {
      return (
        <div> HERE: 
          {this.state.entries}
        </div>
      );
    }
});


// Stylesheet stuff is here, not important for this post.

//Render
var MasterLayout = React.createClass({ 
    render: function(){
        return(
            <html lang="en">
            <head>
                <title>{this.props.name}</title>
            </head>
            <body style={MainStyles.alldivs}>
                <Header />
                <GetStuff />
                {this.props.children}
                <Footer />
            </body>
            </html>
        )   
    }
});


// no idea if this is the correct setup, again docs are lacking on the real use of this.

    if(typeof window !== 'undefined') {
        ReactDom.reder(<MasterLayout />, document.getElementByID("content"));
    }
    module.exports = MasterLayout;
