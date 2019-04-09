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

![](https://i.loli.net/2019/04/09/5cac48663eb5f.png)
