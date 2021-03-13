val arraylist: ArrayList<String> = ArrayList()
        arraylist.add("helo")
        arraylist.add("good")
        val usersSet: Set<String> = HashSet(arraylist)
        val prefs = getSharedPreferences("PREF", MODE_PRIVATE)
        val editor = prefs.edit()
        editor.putStringSet("newusers", usersSet).apply()


        val usersSetget = prefs.getStringSet("newusers", HashSet())
        if (usersSet.contains("heloo")){
            Log.i("dfjkdjfd", "onCreate: yeah it contains")
        }else{
            Log.i("dfjkdjfd", "onCreate:didnt contains")
        }
        Log.i("fksajfksdfjssd", "onCreate:$usersSetget ")
