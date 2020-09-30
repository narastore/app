<?xml version="1.0" encoding="utf-8"?>
<manifest
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:versionCode="521"
    android:versionName="6.1.9"
    android:installLocation="0"
    android:compileSdkVersion="29"
    android:compileSdkVersionCodename="10"
    package="com.obeng"
    platformBuildVersionCode="28"
    platformBuildVersionName="9">

    <uses-sdk
        android:minSdkVersion="14"
        android:targetSdkVersion="29" />

    <uses-feature
        android:name="android.hardware.microphone"
        android:required="false" />

    <uses-permission
        android:name="android.permission.FOREGROUND_SERVICE" />

    <uses-permission
        android:name="android.permission.RECORD_AUDIO" />

    <uses-permission
        android:name="android.permission.INTERNET" />

    <uses-permission
        android:name="android.permission.WRITE_EXTERNAL_STORAGE" />

    <uses-permission
        android:name="android.permission.WAKE_LOCK" />

    <uses-permission
        android:name="android.permission.SYSTEM_ALERT_WINDOW" />

    <uses-permission
        android:name="android.permission.BLUETOOTH" />

    <uses-permission
        android:name="android.permission.ACCESS_NETWORK_STATE" />

    <application
        android:theme="@ref/0x7f100113"
        android:label="@ref/0x7f0f0027"
        android:icon="@ref/0x7f0700b1"
        android:name="androidx.multidex.MultiDexApplication"
        android:allowBackup="true"
        android:appComponentFactory="androidx.core.app.CoreComponentFactory">

        <provider
            android:name="com.rafaci.app.fref.channel.ChannelSearchProvider"
            android:exported="false"
            android:authorities="com.obeng.channel.ChannelSearchProvider" />

        <activity
            android:name="com.rafaci.app.fref.wizard.WizardActivity" />

        <activity
            android:name="com.rafaci.app.fref.preference.Preferences"
            android:parentActivityName="com.rafaci.app.fref.app.MumlaActivity">

            <intent-filter>

                <action
                    android:name="com.rafaci.app.fref.app.PREFS_GENERAL" />

                <category
                    android:name="android.intent.category.DEFAULT" />
            </intent-filter>

            <intent-filter>

                <action
                    android:name="com.rafaci.app.fref.app.PREFS_AUTHENTICATION" />

                <category
                    android:name="android.intent.category.DEFAULT" />
            </intent-filter>

            <intent-filter>

                <action
                    android:name="com.rafaci.app.fref.app.PREFS_AUDIO" />

                <category
                    android:name="android.intent.category.DEFAULT" />
            </intent-filter>

            <intent-filter>

                <action
                    android:name="com.rafaci.app.fref.app.PREFS_APPEARANCE" />

                <category
                    android:name="android.intent.category.DEFAULT" />
            </intent-filter>

            <intent-filter>

                <action
                    android:name="com.rafaci.app.fref.app.PREFS_ABOUT" />

                <category
                    android:name="android.intent.category.DEFAULT" />
            </intent-filter>
        </activity>

        <service
            android:name="com.rafaci.app.fref.service.MumlaService"
            android:enabled="true" />

        <activity
            android:label="@ref/0x7f0f0027"
            android:name="com.rafaci.app.fref.app.MumlaActivity"
            android:launchMode="1">

            <intent-filter>

                <action
                    android:name="android.intent.action.MAIN" />

                <category
                    android:name="android.intent.category.LAUNCHER" />
            </intent-filter>

            <intent-filter>

                <action
                    android:name="android.intent.action.SEARCH" />
            </intent-filter>

            <meta-data
                android:name="android.app.searchable"
                android:resource="@ref/0x7f120002" />

            <intent-filter>

                <action
                    android:name="android.intent.action.VIEW" />

                <category
                    android:name="android.intent.category.DEFAULT" />

                <category
                    android:name="android.intent.category.BROWSABLE" />

                <data
                    android:scheme="mumble" />
            </intent-filter>
        </activity>

        <activity
            android:theme="@ref/0x7f100046"
            android:name="com.rafaci.app.fref.preference.CertificateSelectActivity">

            <intent-filter>

                <action
                    android:name="com.rafaci.app.fref.app.CERTIFICATE_SELECT" />

                <category
                    android:name="android.intent.category.DEFAULT" />
            </intent-filter>
        </activity>

        <activity
            android:theme="@ref/0x7f100046"
            android:name="com.rafaci.app.fref.preference.CertificateImportActivity">

            <intent-filter>

                <action
                    android:name="com.rafaci.app.fref.app.CERTIFICATE_IMPORT" />

                <category
                    android:name="android.intent.category.DEFAULT" />
            </intent-filter>
        </activity>

        <activity
            android:theme="@ref/0x7f100046"
            android:name="com.rafaci.app.fref.preference.CertificateExportActivity">

            <intent-filter>

                <action
                    android:name="com.rafaci.app.fref.app.CERTIFICATE_EXPORT" />

                <category
                    android:name="android.intent.category.DEFAULT" />
            </intent-filter>
        </activity>

        <activity
            android:theme="@ref/0x7f100046"
            android:name="com.rafaci.app.fref.preference.CertificateGenerateActivity">

            <intent-filter>

                <action
                    android:name="com.rafaci.app.fref.app.CERTIFICATE_GENERATE" />

                <category
                    android:name="android.intent.category.DEFAULT" />
            </intent-filter>
        </activity>

        <activity
            android:theme="@ref/0x7f100046"
            android:name="com.rafaci.app.fref.preference.ServerCertificateClearActivity">

            <intent-filter>

                <action
                    android:name="com.rafaci.app.fref.app.CLEAR_SERVER_CERTIFICATES" />

                <category
                    android:name="android.intent.category.DEFAULT" />
            </intent-filter>
        </activity>

        <service
            android:name="se.lublin.humla.HumlaService"
            android:exported="true">

            <intent-filter>

                <action
                    android:name="se.lublin.humla.ACTION_CONNECT" />

                <action
                    android:name="se.lublin.humla.ACTION_DISCONNECT" />
            </intent-filter>
        </service>

        <meta-data
            android:name="com.android.narastore.app"
            android:value="1" />
    </application>
</manifest>
