# Time Wheel Picker [![](https://jitpack.io/v/azizur-rehman/LinkedInAuth.svg)](https://jitpack.io/#azizur-rehman/LinkedInAuth)

A Lightweight android library iOS styled timepicker alongwith range for 24 hour time

Features:
  - Time Range for 24 hours time
  - AM/PM mode
 

Step 1. Add the JitPack repository to your build file

Add it in your root build.gradle at the end of repositories:

	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
  
  
&nbsp;

  Step 2. Add the dependency

	dependencies {
	        implementation 'com.github.azizur-rehman:TimeWheelPicker:{LATEST_VERSION}'
	}
  
  
  &nbsp;
  &nbsp;
 ## Implementation
  
  ### To create a ranged Time Picker
  
         TimeWheelPicker.Builder(context)
                                .setStartTime(startHour, startMin)
                                .setEndTime(endHour, endMin)
                                .setOnTimePickedListener( object : TimeWheelPicker.OnTimePicked{
                                    override fun onPicked(hourOfDay: Int, minute: Int) {
                                        ...
                                        ...
                                    }

                                }
                                ).build()
                                .show()
            
### To create a simple 12 hour based Time Picker
        TimeWheelPicker.Builder(context, is12Hour = true)
                                 .setOnTimePickedListener( object : TimeWheelPicker.OnTimePicked{
                                    override fun onPicked(hourOfDay: Int, minute: Int) {
                                        ...
                                        ...
                                    }

                                }
                                ).build()
                                .show()
      
 
  &nbsp;
  &nbsp;
 ## Available Methods
 
* setConfirmText(text:String)
* setCancelText(text: String)
* setHourTextSize(sizeInPx:Float)
* setMinuteTextSize(sizeInPx: Float)
* setConfirmTextColor(color: Int)
* setCancelTextColor(color: Int)
* setTitle(title:String, color:Int = Color.BLACK)
* setSubtitle(subtitle: String, color:Int = Color.BLACK)

  &nbsp;
  &nbsp;
 ### To Change the wheel or line colors, override these values of your own in your color.xml
    <color name="time_picker_hour_text_color">#000000</color>
    <color name="time_picker_minute_text_color">#000000</color>
    <color name="time_picker_am_pm_text_color">#000000</color>


    <color name="time_picker_hour_text_unselected_color">#ffafafaf</color>
    <color name="time_picker_minute_text_unselected_color">#ffafafaf</color>
    <color name="time_picker_am_pm_text_unselected_color">#ffafafaf</color>


    <color name="time_picker_hour_line_color">@color/colorAccent</color>
    <color name="time_picker_minute_line_color">@color/colorAccent</color>
    <color name="time_picker_am_pm_line_color">@color/colorAccent</color>
  
