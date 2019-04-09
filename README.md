# FragmentPreference

```
<PreferenceCategory android:title="Dialog based preference">
        <EditTextPreference android:key="edit"
            android:title="EditText Preference"
            android:summary="An example that use a EditText"
            android:dialogTitle="Enter your favorite" />
        <ListPreference
            android:key="list"
            android:title="List Preference "
            android:summary="An example that use a ListPreference"
            android:entries="@array/entry_list"
            android:entryValues="@array/values_list"
            android:dialogTitle="Choose One"
            />
    </PreferenceCategory>
```
效果图（EditTextPreference）：

![](https://i.loli.net/2019/04/09/5cac48663eb5f.png)

效果图（ListPreference）：

![](https://i.loli.net/2019/04/09/5cac4901cb4e0.png)

```
 <PreferenceCategory  android:title="Launch preference">
        <PreferenceScreen android:title="Screen preference">
        <CheckBoxPreference
            android:summary="This is a checkbox"
            android:title="CheckBox preference"
            />
        </PreferenceScreen>
        <Preference android:title="intent preference" >
            <intent android:action="android.intent.action.VIEW"
                android:data="http://www.baidu.com" />
        </Preference>
    </PreferenceCategory>
```

效果图（内置CheckBoxPreference）

![](https://i.loli.net/2019/04/09/5cac49b285da6.png)

效果图（intent）

![](https://i.loli.net/2019/04/09/5cac4a8834b11.png)

```
<PreferenceCategory  android:title="Preference attributes">
        <CheckBoxPreference
            android:key="Parent"
            android:summary="This is a visually parent"
            android:title="Parent CheckBox preference"
            />
        <CheckBoxPreference
            android:summary="This is a visually child"
            android:title="Child CheckBox preference"
            android:dependency="Parent"

            />
    </PreferenceCategory>
```
效果图（dependency属性的使用）

![](https://i.loli.net/2019/04/09/5cac4af11abf2.png)

完整代码：

```
<?xml version="1.0" encoding="utf-8"?>
<PreferenceScreen  xmlns:android="http://schemas.android.com/apk/res/android">

<PreferenceCategory  android:title="In-line preference">
    <CheckBoxPreference
        android:summary="This is a checkbox"
        android:title="CheckBox preference"
        />
</PreferenceCategory>

    <PreferenceCategory android:title="Dialog based preference">
        <EditTextPreference android:key="edit"
            android:title="EditText Preference"
            android:summary="An example that use a EditText"
            android:dialogTitle="Enter your favorite" />
        <ListPreference
            android:key="list"
            android:title="List Preference "
            android:summary="An example that use a ListPreference"
            android:entries="@array/entry_list"
            android:entryValues="@array/values_list"
            android:dialogTitle="Choose One"
            />
    </PreferenceCategory>

    <PreferenceCategory  android:title="Launch preference">
        <PreferenceScreen android:title="Screen preference">
        <CheckBoxPreference
            android:summary="This is a checkbox"
            android:title="CheckBox preference"
            />
        </PreferenceScreen>
        <Preference android:title="intent preference" >
            <intent android:action="android.intent.action.VIEW"
                android:data="http://www.baidu.com" />
        </Preference>
    </PreferenceCategory>
    <PreferenceCategory  android:title="Preference attributes">
        <CheckBoxPreference
            android:key="Parent"
            android:summary="This is a visually parent"
            android:title="Parent CheckBox preference"
            />
        <CheckBoxPreference
            android:summary="This is a visually child"
            android:title="Child CheckBox preference"
            android:dependency="Parent"

            />
    </PreferenceCategory>
</PreferenceScreen>
```
