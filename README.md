# Program-Assignment-2
// this sets the background color of the master UIView (when there are no windows/tab groups on it)
Titanium.UI.setBackgroundColor('#000');

// create tab group
var tabGroup = Titanium.UI.createTabGroup();


//
// create base UI tab and root window
//
var win1 = Titanium.UI.createWindow({  
    title:'Go Vandals!',
    backgroundColor:'#2ECCFA'
});
var tab1 = Titanium.UI.createTab({  
    icon:'KS_nav_views.png',
    title:'Go Vandals!',
    window:win1
});

var label1 = Titanium.UI.createLabel({
	color:'#4B088A',
	text:'This is a Vandals Fan Page',
	font:{fontSize:20,fontFamily:'Georgia'},
	textAlign:'center',
	width:'auto'
});

win1.add(label1);

//
// create controls tab and root window
//
var win2 = Titanium.UI.createWindow({  
    title:'University of Idaho',
    backgroundColor:'#FE2EF7'
});
var tab2 = Titanium.UI.createTab({  
    icon:'KS_nav_ui.png',
    title:'University of Idaho',
    window:win2
});

var label2 = Titanium.UI.createLabel({
	color:'#240B3B',
	text:'Who do we hate? BSU',
	font:{fontSize:20,fontFamily:'Georgia'},
	textAlign:'center',
	width:'auto'
});

win2.add(label2);



//
//  add tabs
//
tabGroup.addTab(tab1);  
tabGroup.addTab(tab2);  


// open tab group
tabGroup.open();
