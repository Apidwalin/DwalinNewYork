# DwalinNewYork
DwalinNewYork
<!DOCTYPE html>
<!-- saved from url=(0027)http://localhost:5001/tree# -->
<html lang="th-th"><head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
    

    <title>Home Page - Select or create a notebook</title>
    <link id="favicon" rel="shortcut icon" type="image/x-icon" href="http://localhost:5001/static/base/images/favicon.ico?v=50afa725b5de8b00030139d09b38620224d4e7dba47c07ef0e86d4643f30c9bfe6bb7e1a4a1c561aa32834480909a4b6fe7cd1e17f7159330b6b5914bf45a880">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <link rel="stylesheet" href="./Home Page - Select or create a notebook_files/jquery-ui.min.css" type="text/css">
    <link rel="stylesheet" href="./Home Page - Select or create a notebook_files/jquery.typeahead.min.css" type="text/css">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    
    <link rel="stylesheet" href="./Home Page - Select or create a notebook_files/style.min.css" type="text/css">
    
    <link rel="stylesheet" href="./Home Page - Select or create a notebook_files/custom.css" type="text/css">
    <script src="./Home Page - Select or create a notebook_files/promise.min.js.download" type="text/javascript" charset="utf-8"></script>
    <script src="./Home Page - Select or create a notebook_files/react.production.min.js.download" type="text/javascript"></script>
    <script src="./Home Page - Select or create a notebook_files/react-dom.production.min.js.download" type="text/javascript"></script>
    <script src="./Home Page - Select or create a notebook_files/index.js.download" type="text/javascript"></script>
    <script src="./Home Page - Select or create a notebook_files/require.js.download" type="text/javascript" charset="utf-8"></script>
    <script>
      require.config({
          
          urlArgs: "v=20210610132001",
          
          baseUrl: '/static/',
          paths: {
            'auth/js/main': 'auth/js/main.min',
            custom : '/custom',
            nbextensions : '/nbextensions',
            kernelspecs : '/kernelspecs',
            underscore : 'components/underscore/underscore-min',
            backbone : 'components/backbone/backbone-min',
            jed: 'components/jed/jed',
            jquery: 'components/jquery/jquery.min',
            json: 'components/requirejs-plugins/src/json',
            text: 'components/requirejs-text/text',
            bootstrap: 'components/bootstrap/dist/js/bootstrap.min',
            bootstraptour: 'components/bootstrap-tour/build/js/bootstrap-tour.min',
            'jquery-ui': 'components/jquery-ui/jquery-ui.min',
            moment: 'components/moment/min/moment-with-locales',
            codemirror: 'components/codemirror',
            termjs: 'components/xterm.js/xterm',
            typeahead: 'components/jquery-typeahead/dist/jquery.typeahead.min',
          },
          map: { // for backward compatibility
              "*": {
                  "jqueryui": "jquery-ui",
              }
          },
          shim: {
            typeahead: {
              deps: ["jquery"],
              exports: "typeahead"
            },
            underscore: {
              exports: '_'
            },
            backbone: {
              deps: ["underscore", "jquery"],
              exports: "Backbone"
            },
            bootstrap: {
              deps: ["jquery"],
              exports: "bootstrap"
            },
            bootstraptour: {
              deps: ["bootstrap"],
              exports: "Tour"
            },
            "jquery-ui": {
              deps: ["jquery"],
              exports: "$"
            }
          },
          waitSeconds: 30,
      });

      require.config({
          map: {
              '*':{
                'contents': 'services/contents',
              }
          }
      });

      // error-catching custom.js shim.
      define("custom", function (require, exports, module) {
          try {
              var custom = require('custom/custom');
              console.debug('loaded custom.js');
              return custom;
          } catch (e) {
              console.error("error loading custom.js", e);
              return {};
          }
      })

    document.nbjs_translations = {"domain": "nbjs", "locale_data": {"nbjs": {"": {"domain": "nbjs"}}}};
    document.documentElement.lang = navigator.language.toLowerCase();
    </script>

    
    

<script type="text/javascript" charset="utf-8" async="" data-requirecontext="_" data-requiremodule="services/contents" src="./Home Page - Select or create a notebook_files/contents.js.download"></script><script type="text/javascript" charset="utf-8" async="" data-requirecontext="_" data-requiremodule="custom/custom" src="./Home Page - Select or create a notebook_files/custom.js.download"></script></head>

<body class="" data-jupyter-api-token="d51f9bc0c3a817bdad144643cd8ef8d82982c32a4651183e" data-base-url="/" data-notebook-path="" data-terminals-available="True" data-server-root="C:\tensorflow1\research" dir="ltr">

<noscript>
    <div id='noscript'>
      Jupyter Notebook requires JavaScript.<br>
      Please enable it to proceed. 
  </div>
</noscript>

<div id="header" role="navigation" aria-label="Top Menu" style="display: block;">
  <div id="header-container" class="container">
  <div id="ipython_notebook" class="nav navbar-brand"><a href="http://localhost:5001/tree?token=d51f9bc0c3a817bdad144643cd8ef8d82982c32a4651183e" title="dashboard">
      <img src="./Home Page - Select or create a notebook_files/logo.png" alt="Jupyter Notebook">
  </a></div>

  
  <span class="flex-spacer"></span>
  
  
  
    <span id="shutdown_widget">
      <button id="shutdown" class="btn btn-sm navbar-btn" title="Stop the Jupyter server">
          Quit
      </button>
    </span>
  

  
  
  
  

    <span id="login_widget">
      
        <button id="logout" class="btn btn-sm navbar-btn">Logout</button>
      
    </span>

  

  
  
  </div>
  <div class="header-bar"></div>

  
  
</div>

<div id="site" style="display: block; height: 640px;">


  <div id="ipython-main-app" class="container">
    <div id="tab_content" class="tabbable" role="main">
      <ul id="tabs" class="nav nav-tabs">
        <li class="active"><a href="http://localhost:5001/tree#notebooks" data-toggle="tab">Files</a></li>
        <li><a href="http://localhost:5001/tree#running" data-toggle="tab">Running</a></li>
        <li><a href="http://localhost:5001/tree#clusters" data-toggle="tab" class="clusters_tab_link">Clusters</a></li>
      </ul>
      <div class="tab-content">
        <div id="notebooks" class="tab-pane active">
          <div id="notebook_toolbar" class="row list_toolbar">
            <div class="col-sm-8 no-padding">
              <div class="dynamic-instructions">
                Select items to perform actions on them.
              </div>
              <div class="dynamic-buttons">
                  <button title="Duplicate selected" aria-label="Duplicate selected" class="duplicate-button btn btn-default btn-xs" aria-describedby="tooltip1" style="display: none;">Duplicate </button>
                  <div role="tooltip" id="tooltip1">Duplicate selected</div>
                  <button title="Rename selected" aria-label="Rename selected" class="rename-button btn btn-default btn-xs" aria-describedby="tooltip2" style="display: none;">Rename</button>
                  <div role="tooltip" id="tooltip2">Rename selected</div> 
                  <button title="Move selected" aria-label="Move selected" class="move-button btn btn-default btn-xs" aria-describedby="tooltip3" style="display: none;">Move</button>
                  <div role="tooltip" id="tooltip3">Move selected</div> 
                  <button title="Download selected" aria-label="Download selected" class="download-button btn btn-default btn-xs" aria-describedby="tooltip4" style="display: none;">Download</button>
                  <div role="tooltip" id="tooltip4">Download selected</div>
                  <button title="Shutdown selected notebook(s)" aria-label="Shutdown selected notebook(s)" class="shutdown-button btn btn-default btn-xs btn-warning" aria-describedby="tooltip5" style="display: none;">Shutdown</button>
                  <div role="tooltip" id="tooltip5">Shutdown selected notebook(s)</div>  
                  <button title="View selected" aria-label="View selected" class="view-button btn btn-default btn-xs" aria-describedby="tooltip6" style="display: none;">View</button>
                  <div role="tooltip" id="tooltip6">View selected</div> 
                  <button title="Edit selected" aria-label="Edit selected" class="edit-button btn btn-default btn-xs" aria-describedby="tooltip7" style="display: none;">Edit</button>
                  <div role="tooltip" id="tooltip7">Edit selected</div>  
                  <button title="Delete selected" aria-label="Delete selected" class="delete-button btn btn-default btn-xs btn-danger" aria-describedby="tooltip8" style="display: none;">
                    <i class="fa fa-trash"></i>
                  </button>
                  <div role="tooltip" id="tooltip8">Delete selected</div>
              </div>
            </div>
            <div class="col-sm-4 no-padding tree-buttons">
              <div class="pull-right">
                <form id="alternate_upload" class="alternate_upload">
                  <span id="notebook_list_info" class="toolbar_info">
                  <span id="upload_span" class="btn btn-xs btn-default btn-upload" role="button" tabindex="0">
                    <input id="upload_span_input" title="Click to browse for a file to upload." type="file" name="datafile" class="fileinput" multiple="multiple" tabindex="-1">
                    Upload
                  </span>
                  </span>
                </form>
                <div id="new-buttons" class="btn-group">
                  <button class="dropdown-toggle btn btn-default btn-xs" id="new-dropdown-button" data-toggle="dropdown">
                  <span>New</span>
                  <span class="caret"></span>
                  <span class="sr-only">Toggle Dropdown</span>
                  </button>
                  <ul id="new-menu" class="dropdown-menu" role="menu">
                    <li role="menuitem" class="dropdown-header" id="notebook-kernels">Notebook:</li><li id="kernel-python3"><a aria-label="python3" role="menuitem" href="http://localhost:5001/tree#" title="Create a new notebook with Python 3">Python 3</a></li>
                    <li role="presentation" class="divider"></li>
                    <li role="menuitem" class="dropdown-header">Other:</li>
                    <li role="none" id="new-file">
                        <a role="menuitem" tabindex="-1" href="http://localhost:5001/tree#">Text File</a>
                    </li>
                    <li role="none" id="new-folder">
                        <a role="menuitem" tabindex="-1" href="http://localhost:5001/tree#">Folder</a>
                    </li>
                    
                    <li role="none" id="new-terminal">
                        <a role="menuitem" tabindex="-1" href="http://localhost:5001/tree#">Terminal</a>
                    </li>
                    
                  </ul>
                </div>
                <div class="btn-group">
                    <button id="refresh_notebook_list" title="Refresh notebook list" aria-label="Refresh notebook list" class="btn btn-default btn-xs"><i class="fa fa-refresh"></i></button>
                </div>
              </div>
            </div>
          </div>
          <div id="notebook_list" class="list_container">
            <div id="notebook_list_header" class="row list_header">
              <div class="btn-group dropdown" id="tree-selector">
                <button title="Select All / None" aria-label="Select All/None" type="button" class="btn btn-default btn-xs" id="button-select-all" role="checkbox">
                  <input type="checkbox" class="pull-left tree-selector" id="select-all" tabindex="-1"><span id="counter-select-all">0</span>
                </button>
                <button title="Select Folders/All Notebooks/Running/Files" class="btn btn-default btn-xs dropdown-toggle" type="button" id="tree-selector-btn" data-toggle="dropdown" aria-expanded="true">
                  <span class="sr-only">checkbox</span>
                  <span class="caret"></span>
                  <span class="sr-only">Toggle Dropdown</span>
                </button>
                <ul id="selector-menu" class="dropdown-menu" role="menu" aria-labelledby="tree-selector-btn">
                  <li role="none"><a id="select-folders" role="menuitem" tabindex="-1" href="http://localhost:5001/tree#" title="Select All Folders"><i class="menu_icon folder_icon icon-fixed-width"></i>&nbsp;Folders</a></li>
                  <li role="none"><a id="select-notebooks" role="menuitem" tabindex="-1" href="http://localhost:5001/tree#" title="Select All Notebooks"><i class="menu_icon notebook_icon icon-fixed-width"></i>&nbsp;All Notebooks</a></li>
                  <li role="none"><a id="select-running-notebooks" role="menuitem" tabindex="-1" href="http://localhost:5001/tree#" title="Select Running Notebooks"><i class="menu_icon running_notebook_icon icon-fixed-width"></i>&nbsp;Running</a></li>
                  <li role="none"><a id="select-files" role="menuitem" tabindex="-1" href="http://localhost:5001/tree#" title="Select All Files"><i class="menu_icon file_icon icon-fixed-width"></i>&nbsp;Files</a></li>
                </ul>
              </div>
              <div id="project_name">
                <ul class="breadcrumb"><li><a href="http://localhost:5001/tree" title="Link to root folder"><i class="fa fa-folder"></i></a></li><li><a href="http://localhost:5001/tree"></a></li></ul>
              </div>
              <div id="sort_buttons" class="pull-right">
                <div id="sort_name" class="sort_button">
                  <button type="button" class="btn btn-xs btn-default sort-action" id="sort-name" aria-label="Sort by name">
                        Name
                        <i class="fa fa-arrow-down"></i>
                  </button>
                </div>
                <div id="last_modified" class="sort_button">
                    <button type="button" class="btn btn-xs btn-default sort-action" id="last-modified" aria-label="Sort by last modified">
                        Last Modified
                        <i class="fa"></i>
                    </button>
                </div>
                <div id="file_size" class="sort_button">
                    <button type="button" class="btn btn-xs btn-default sort-action" id="file-size" aria-label="Sort by file size">
                        File size
                        <i class="fa"></i>
                    </button>
                </div>
              </div>
            </div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon folder_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/tree/a3c_blogpost"><span class="item_name">a3c_blogpost</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="visibility: hidden;">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 02:37">11 ชั่วโมงที่แล้ว</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon folder_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/tree/adversarial_text"><span class="item_name">adversarial_text</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="visibility: hidden;">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 02:37">11 ชั่วโมงที่แล้ว</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon folder_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/tree/attention_ocr"><span class="item_name">attention_ocr</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="visibility: hidden;">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 02:37">11 ชั่วโมงที่แล้ว</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon folder_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/tree/audioset"><span class="item_name">audioset</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="visibility: hidden;">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 02:37">11 ชั่วโมงที่แล้ว</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon folder_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/tree/autoaugment"><span class="item_name">autoaugment</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="visibility: hidden;">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 02:37">11 ชั่วโมงที่แล้ว</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon folder_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/tree/build"><span class="item_name">build</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="visibility: hidden;">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 02:37">11 ชั่วโมงที่แล้ว</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon folder_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/tree/cognitive_planning"><span class="item_name">cognitive_planning</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="visibility: hidden;">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 02:37">11 ชั่วโมงที่แล้ว</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon folder_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/tree/cvt_text"><span class="item_name">cvt_text</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="visibility: hidden;">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 02:37">11 ชั่วโมงที่แล้ว</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon folder_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/tree/deep_speech"><span class="item_name">deep_speech</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="visibility: hidden;">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 02:38">11 ชั่วโมงที่แล้ว</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon folder_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/tree/deeplab"><span class="item_name">deeplab</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="visibility: hidden;">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 02:37">11 ชั่วโมงที่แล้ว</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon folder_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/tree/delf"><span class="item_name">delf</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="visibility: hidden;">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 02:38">11 ชั่วโมงที่แล้ว</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon folder_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/tree/dist"><span class="item_name">dist</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="visibility: hidden;">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 02:37">11 ชั่วโมงที่แล้ว</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon folder_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/tree/efficient-hrl"><span class="item_name">efficient-hrl</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="visibility: hidden;">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-03-30 18:26">2 เดือนที่แล้ว</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon folder_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/tree/lfads"><span class="item_name">lfads</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="visibility: hidden;">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-03-30 18:26">2 เดือนที่แล้ว</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon folder_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/tree/lstm_object_detection"><span class="item_name">lstm_object_detection</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="visibility: hidden;">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-03-30 18:26">2 เดือนที่แล้ว</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon folder_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/tree/marco"><span class="item_name">marco</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="visibility: hidden;">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-03-30 18:26">2 เดือนที่แล้ว</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon folder_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/tree/nst_blogpost"><span class="item_name">nst_blogpost</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="visibility: hidden;">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-03-30 18:26">2 เดือนที่แล้ว</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon folder_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/tree/object_detection"><span class="item_name">object_detection</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="visibility: hidden;">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 08:32">5 ชั่วโมงที่แล้ว</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon folder_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/tree/object_detection.egg-info"><span class="item_name">object_detection.egg-info</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="visibility: hidden;">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 11:57">2 ชั่วโมงที่แล้ว</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon folder_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/tree/pcl_rl"><span class="item_name">pcl_rl</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="visibility: hidden;">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-03-30 18:26">2 เดือนที่แล้ว</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon folder_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/tree/pycocotools"><span class="item_name">pycocotools</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="visibility: hidden;">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-03-30 18:26">2 เดือนที่แล้ว</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon folder_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/tree/rebar"><span class="item_name">rebar</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="visibility: hidden;">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-03-30 18:26">2 เดือนที่แล้ว</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon folder_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/tree/seq_flow_lite"><span class="item_name">seq_flow_lite</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="visibility: hidden;">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 02:49">11 ชั่วโมงที่แล้ว</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon folder_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/tree/sequence_projection"><span class="item_name">sequence_projection</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="visibility: hidden;">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-03-30 18:26">2 เดือนที่แล้ว</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon folder_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/tree/slim"><span class="item_name">slim</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="visibility: hidden;">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 02:49">11 ชั่วโมงที่แล้ว</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon folder_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/tree/Untitled%20Folder"><span class="item_name">Untitled Folder</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="visibility: hidden;">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 13:20">13 นาทีที่แล้ว</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon folder_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/tree/vid2depth"><span class="item_name">vid2depth</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="visibility: hidden;">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-03-30 18:26">2 เดือนที่แล้ว</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon running_notebook_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/notebooks/centernet_on_device-checkpoint-checkpoint.ipynb" target="_blank"><span class="item_name">centernet_on_device-checkpoint-checkpoint.ipynb</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 13:26">8 นาทีที่แล้ว</span><span class="file_size pull-right">36.6 kB</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon running_notebook_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/notebooks/centernet_on_device-checkpoint.ipynb" target="_blank"><span class="item_name">centernet_on_device-checkpoint.ipynb</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 13:31">3 นาทีที่แล้ว</span><span class="file_size pull-right">36.7 kB</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon running_notebook_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/notebooks/context_rcnn_tutorial-checkpoint.ipynb" target="_blank"><span class="item_name">context_rcnn_tutorial-checkpoint.ipynb</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 13:31">3 นาทีที่แล้ว</span><span class="file_size pull-right">60.7 kB</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon running_notebook_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/notebooks/customize_encoder.ipynb" target="_blank"><span class="item_name">customize_encoder.ipynb</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 13:31">3 นาทีที่แล้ว</span><span class="file_size pull-right">32.4 kB</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon running_notebook_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/notebooks/decoding_api_in_tf_nlp.ipynb" target="_blank"><span class="item_name">decoding_api_in_tf_nlp.ipynb</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 13:31">3 นาทีที่แล้ว</span><span class="file_size pull-right">49.8 kB</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon running_notebook_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/notebooks/nlp_modeling_library_intro-checkpoint.ipynb" target="_blank"><span class="item_name">nlp_modeling_library_intro-checkpoint.ipynb</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 13:31">2 นาทีที่แล้ว</span><span class="file_size pull-right">30.1 kB</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon running_notebook_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/notebooks/nlp_modeling_library_intro.ipynb" target="_blank"><span class="item_name">nlp_modeling_library_intro.ipynb</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 13:31">2 นาทีที่แล้ว</span><span class="file_size pull-right">31.1 kB</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon running_notebook_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/notebooks/object_detection_tutorial-checkpoint.ipynb" target="_blank"><span class="item_name">object_detection_tutorial-checkpoint.ipynb</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 13:33">ไม่กี่วินาทีที่แล้ว</span><span class="file_size pull-right">42.4 kB</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon file_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/edit/README.md" target="_blank"><span class="item_name">README.md</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="visibility: hidden;">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2020-09-19 10:56">9 เดือนที่แล้ว</span><span class="file_size pull-right">7.13 kB</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><input type="checkbox" title="Click here to rename, delete, etc."><i class="item_icon file_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/edit/setup.py" target="_blank"><span class="item_name">setup.py</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="running-indicator" style="visibility: hidden;">Running</div></div><div class="pull-right"><span class="item_modified pull-left" title="2020-09-19 10:56">9 เดือนที่แล้ว</span><span class="file_size pull-right">446 B</span></div></div></div></div>
          </div>
        </div>
        <div id="running" class="tab-pane">
          <div id="running_toolbar" class="row list_toolbar">
            <div class="col-sm-8 no-padding">
              <span id="running_list_info" class="toolbar_info">Currently running Jupyter processes</span>
            </div>
            <div class="col-sm-4 no-padding tree-buttons">
              <span id="running_buttons" class="pull-right toolbar_buttons">
              <button id="refresh_running_list" title="Refresh running list" aria-label="Refresh running list" class="btn btn-default btn-xs"><i class="fa fa-refresh"></i></button>
              </span>
            </div>
          </div>
          <div class="panel-group" id="accordion">
            <div class="panel panel-default">
              <div class="panel-heading">
                <a data-toggle="collapse" data-target="#collapseOne" href="http://localhost:5001/tree#">
                  Terminals
                <i class="fa fa-caret-down"></i></a>
              </div>
              <div id="collapseOne" class=" collapse in">
                <div class="panel-body">
                  <div id="terminal_list" class="list_container">
                    <div id="terminal_list_header" class="row list_placeholder">
                    
                      <div> There are no terminals running. </div>
                    
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div class="panel panel-default">
              <div class="panel-heading">
                <a data-toggle="collapse" data-target="#collapseTwo" href="http://localhost:5001/tree#">
                  Notebooks
                <i class="fa fa-caret-down"></i></a>
              </div>
              <div id="collapseTwo" class=" collapse in">
                <div class="panel-body">
                  <div id="running_list" class="list_container">
                    <div id="running_list_placeholder" class="row list_placeholder" style="display: none;">
                      <div> There are no notebooks running. </div>
                    </div>
                  <div class="list_item row"><div class="col-md-12"><i class="item_icon running_notebook_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/notebooks/centernet_on_device-checkpoint-checkpoint.ipynb" target="_blank"><span class="item_name">centernet_on_device-checkpoint-checkpoint.ipynb</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="kernel-name">Python 3</div><button class="btn btn-warning btn-xs">Shutdown</button></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 13:34">seconds ago</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><i class="item_icon running_notebook_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/notebooks/centernet_on_device-checkpoint.ipynb" target="_blank"><span class="item_name">centernet_on_device-checkpoint.ipynb</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="kernel-name">Python 3</div><button class="btn btn-warning btn-xs">Shutdown</button></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 13:34">seconds ago</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><i class="item_icon running_notebook_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/notebooks/context_rcnn_tutorial-checkpoint.ipynb" target="_blank"><span class="item_name">context_rcnn_tutorial-checkpoint.ipynb</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="kernel-name">Python 3</div><button class="btn btn-warning btn-xs">Shutdown</button></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 13:34">seconds ago</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><i class="item_icon running_notebook_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/notebooks/customize_encoder.ipynb" target="_blank"><span class="item_name">customize_encoder.ipynb</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="kernel-name">Python 3</div><button class="btn btn-warning btn-xs">Shutdown</button></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 13:34">seconds ago</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><i class="item_icon running_notebook_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/notebooks/decoding_api_in_tf_nlp.ipynb" target="_blank"><span class="item_name">decoding_api_in_tf_nlp.ipynb</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="kernel-name">Python 3</div><button class="btn btn-warning btn-xs">Shutdown</button></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 13:34">seconds ago</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><i class="item_icon running_notebook_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/notebooks/nlp_modeling_library_intro.ipynb" target="_blank"><span class="item_name">nlp_modeling_library_intro.ipynb</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="kernel-name">Python 3</div><button class="btn btn-warning btn-xs">Shutdown</button></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 13:34">seconds ago</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><i class="item_icon running_notebook_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/notebooks/nlp_modeling_library_intro-checkpoint.ipynb" target="_blank"><span class="item_name">nlp_modeling_library_intro-checkpoint.ipynb</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="kernel-name">Python 3</div><button class="btn btn-warning btn-xs">Shutdown</button></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 13:34">seconds ago</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div><div class="list_item row"><div class="col-md-12"><i class="item_icon running_notebook_icon icon-fixed-width"></i><a class="item_link" href="http://localhost:5001/notebooks/object_detection_tutorial-checkpoint.ipynb" target="_blank"><span class="item_name">object_detection_tutorial-checkpoint.ipynb</span></a><div class="pull-right"><div class="item_buttons pull-left"><div class="kernel-name">Python 3</div><button class="btn btn-warning btn-xs">Shutdown</button></div><div class="pull-right"><span class="item_modified pull-left" title="2021-06-10 13:34">seconds ago</span><span class="file_size pull-right">&nbsp;</span></div></div></div></div></div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div id="clusters" class="tab-pane">
          Clusters tab is now provided by IPython parallel.
          See '<a href="https://github.com/ipython/ipyparallel">IPython parallel</a>' for installation details.
        </div>
      </div><!-- class:tab-content -->
    </div><!-- id:tab_content -->
  </div><!-- ipython-main-app  -->


</div>





    

    <script type="text/javascript">
      ('#element').tooltip('enable')
    </script>

<script src="./Home Page - Select or create a notebook_files/main.min.js.download" type="text/javascript" charset="utf-8"></script>



<script type="text/javascript">
  function _remove_token_from_url() {
    if (window.location.search.length <= 1) {
      return;
    }
    var search_parameters = window.location.search.slice(1).split('&');
    for (var i = 0; i < search_parameters.length; i++) {
      if (search_parameters[i].split('=')[0] === 'token') {
        // remote token from search parameters
        search_parameters.splice(i, 1);
        var new_search = '';
        if (search_parameters.length) {
          new_search = '?' + search_parameters.join('&');
        }
        var new_url = window.location.origin + 
                      window.location.pathname + 
                      new_search + 
                      window.location.hash;
        window.history.replaceState({}, "", new_url);
        return;
      }
    }
  }
  _remove_token_from_url();
</script>


</body></html>
