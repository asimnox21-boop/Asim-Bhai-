ASIMOfficial/
├── settings.gradle.kts
├── build.gradle.kts
└── app/
    ├── build.gradle.kts
    └── src/main/
        ├── AndroidManifest.xml
        ├── java/com/asimofficial/gameutility/
        │   ├── ui/
        │   │   ├── LoginActivity.kt
        │   │   ├── HomeActivity.kt
        │   │   └── GameAdapter.kt
        │   ├── service/
        │   │   └── OverlayService.kt
        │   ├── data/
        │   │   ├── LicenseRepository.kt
        │   │   └── SessionManager.kt
        │   ├── model/
        │   │   └── GameApp.kt
        │   └── util/
        │       └── GameDetector.kt
        └── res/
            ├── layout/
            │   ├── activity_login.xml
            │   ├── activity_home.xml
            │   ├── item_game.xml
            │   └── overlay_view.xml
            ├── drawable/
            │   ├── bg_app.xml
            │   ├── bg_button.xml
            │   ├── bg_game_item.xml
            │   ├── bg_overlay.xml
            │   ├── bg_overlay_lock.xml
            │   ├── bg_qr.xml
            │   ├── ic_add.xml
            │   ├── ic_game.xml
            │   ├── ic_lock.xml
            │   ├── ic_unlock.xml
            │   └── ic_launcher_foreground.xml
            └── values/
                ├── colors.xml
                ├── strings.xml
                └── themes.xml
pluginManagement {
    repositories {
        google()
        mavenCentral()
        gradlePluginPortal()
    }
}

dependencyResolutionManagement {
    repositoriesMode.set(
        RepositoriesMode.FAIL_ON_PROJECT_REPOS
    )

    repositories {
        google()
        mavenCentral()
    }
}

rootProject.name = "ASIMOfficial"

include(":app")
plugins {
    id("com.android.application") version "8.7.3" apply false
    id("org.jetbrains.kotlin.android") version "2.0.21" apply false
    id("com.google.gms.google-services") version "4.4.2" apply false
}
plugins {
    id("com.android.application")
    id("org.jetbrains.kotlin.android")
    id("com.google.gms.google-services")
}

android {
    namespace = "com.asimofficial.gameutility"

    compileSdk = 35

    defaultConfig {
        applicationId = "com.asimofficial.gameutility"

        minSdk = 31
        targetSdk = 35

        versionCode = 1
        versionName = "1.0.0"
    }

    buildFeatures {
        viewBinding = true
    }

    compileOptions {
        sourceCompatibility = JavaVersion.VERSION_17
        targetCompatibility = JavaVersion.VERSION_17
    }

    kotlinOptions {
        jvmTarget = "17"
    }
}

dependencies {

    implementation(
        "androidx.core:core-ktx:1.15.0"
    )

    implementation(
        "androidx.appcompat:appcompat:1.7.0"
    )

    implementation(
        "androidx.activity:activity-ktx:1.10.1"
    )

    implementation(
        "androidx.lifecycle:lifecycle-runtime-ktx:2.8.7"
    )

    implementation(
        "androidx.recyclerview:recyclerview:1.4.0"
    )

    implementation(
        "com.google.android.material:material:1.12.0"
    )

    implementation(
        "androidx.security:security-crypto:1.1.0-alpha06"
    )

    implementation(
        "org.jetbrains.kotlinx:kotlinx-coroutines-android:1.9.0"
    )

    implementation(
        "com.google.firebase:firebase-database-ktx:21.0.0"
    )

    implementation(
        "com.google.firebase:firebase-auth-ktx:23.1.0"
    )
}
<?xml version="1.0" encoding="utf-8"?>

<manifest
    xmlns:android="http://schemas.android.com/apk/res/android">

    <uses-permission
        android:name="android.permission.INTERNET" />

    <uses-permission
        android:name="android.permission.SYSTEM_ALERT_WINDOW" />

    <uses-permission
        android:name="android.permission.FOREGROUND_SERVICE" />

    <uses-permission
        android:name="android.permission.FOREGROUND_SERVICE_SPECIAL_USE" />

    <uses-permission
        android:name="android.permission.QUERY_ALL_PACKAGES" />

    <application
        android:name=".ASIMApplication"
        android:allowBackup="false"
        android:fullBackupContent="false"
        android:icon="@drawable/ic_game"
        android:label="@string/app_name"
        android:supportsRtl="true"
        android:theme="@style/Theme.ASIMOfficial">

        <activity
            android:name=".ui.HomeActivity"
            android:exported="false" />

        <activity
            android:name=".ui.LoginActivity"
            android:exported="true">

            <intent-filter>

                <action
                    android:name="android.intent.action.MAIN" />

                <category
                    android:name="android.intent.category.LAUNCHER" />

            </intent-filter>

        </activity>

        <service
            android:name=".service.OverlayService"
            android:exported="false"
            android:foregroundServiceType="specialUse">

            <property
                android:name="android.app.PROPERTY_SPECIAL_USE_FGS_SUBTYPE"
                android:value="game_overlay" />

        </service>

    </application>

</manifest>
package com.asimofficial.gameutility

import android.app.Application
import com.google.firebase.FirebaseApp

class ASIMApplication : Application() {

    override fun onCreate() {
        super.onCreate()

        FirebaseApp.initializeApp(this)
    }
}
package com.asimofficial.gameutility.model

import android.graphics.drawable.Drawable

data class GameApp(
    val packageName: String,
    val appName: String,
    val icon: Drawable,
    val isManuallyAdded: Boolean = false
)
package com.asimofficial.gameutility.data

import android.content.Context
import androidx.security.crypto.EncryptedSharedPreferences
import androidx.security.crypto.MasterKey

class SessionManager(
    context: Context
) {

    companion object {
        private const val FILE_NAME =
            "asim_official_secure_session"

        private const val KEY_LOGGED_IN =
            "logged_in"

        private const val KEY_REDEEM_CODE =
            "redeem_code"
    }

    private val masterKey =
        MasterKey.Builder(context)
            .setKeyScheme(
                MasterKey.KeyScheme.AES256_GCM
            )
            .build()

    private val preferences =
        EncryptedSharedPreferences.create(
            context,
            FILE_NAME,
            masterKey,
            EncryptedSharedPreferences.PrefKeyEncryptionScheme.AES256_SIV,
            EncryptedSharedPreferences.PrefValueEncryptionScheme.AES256_GCM
        )

    fun isLoggedIn(): Boolean {
        return preferences.getBoolean(
            KEY_LOGGED_IN,
            false
        )
    }

    fun saveSession(code: String) {
        preferences.edit()
            .putBoolean(KEY_LOGGED_IN, true)
            .putString(KEY_REDEEM_CODE, code)
            .apply()
    }

    fun getRedeemCode(): String? {
        return preferences.getString(
            KEY_REDEEM_CODE,
            null
        )
    }

    fun clearSession() {
        preferences.edit()
            .clear()
            .apply()
    }
}
package com.asimofficial.gameutility.data

import com.google.firebase.database.DatabaseReference
import com.google.firebase.database.FirebaseDatabase
import com.google.firebase.database.MutableData
import com.google.firebase.database.Transaction
import kotlinx.coroutines.tasks.await

sealed class LicenseResult {

    data object Success : LicenseResult()

    data object InvalidCode : LicenseResult()

    data object AlreadyBound : LicenseResult()

    data object Expired : LicenseResult()

    data object Disabled : LicenseResult()

    data class Error(
        val message: String
    ) : LicenseResult()
}

class LicenseRepository {

    private val database: DatabaseReference =
        FirebaseDatabase
            .getInstance()
            .reference
            .child("redeemCodes")

    suspend fun redeemCode(
        code: String,
        deviceId: String
    ): LicenseResult {

        val normalizedCode =
            code.trim().uppercase()

        if (normalizedCode.isBlank()) {
            return LicenseResult.InvalidCode
        }

        return try {

            val result =
                database
                    .child(normalizedCode)
                    .runTransaction(
                        object :
                            Transaction.Handler {

                            override fun doTransaction(
                                currentData: MutableData
                            ): Transaction.Result {

                                if (!currentData.exists()) {
                                    return Transaction.abort()
                                }

                                val value =
                                    currentData.value
                                        as? Map<*, *>
                                        ?: return Transaction.abort()

                                val enabled =
                                    value["enabled"]
                                        as? Boolean
                                        ?: false

                                if (!enabled) {
                                    return Transaction.abort()
                                }

                                val expiresAt =
                                    when (
                                        val raw =
                                            value["expiresAt"]
                                    ) {
                                        is Long -> raw
                                        is Double ->
                                            raw.toLong()
                                        is Int ->
                                            raw.toLong()
                                        else -> 0L
                                    }

                                if (
                                    expiresAt > 0L &&
                                    System.currentTimeMillis() >
                                    expiresAt
                                ) {
                                    return Transaction.abort()
                                }

                                val existingDevice =
                                    value["deviceId"]
                                        as? String

                                if (
                                    !existingDevice.isNullOrBlank() &&
                                    existingDevice != deviceId
                                ) {
                                    return Transaction.abort()
                                }

                                if (
                                    existingDevice ==
                                    deviceId
                                ) {
                                    return Transaction.abort()
                                }

                                val updated =
                                    HashMap(
                                        value
                                    )

                                updated["deviceId"] =
                                    deviceId

                                updated["redeemed"] =
                                    true

                                updated["redeemedAt"] =
                                    System.currentTimeMillis()

                                currentData.value =
                                    updated

                                return Transaction.success(
                                    currentData
                                )
                            }

                            override fun onComplete(
                                error: com.google.firebase.database.DatabaseError?,
                                committed: Boolean,
                                currentData: com.google.firebase.database.DataSnapshot?
                            ) {
                            }
                        }
                    )
                    .await()

            if (!result.committed) {

                val snapshot =
                    database
                        .child(normalizedCode)
                        .get()
                        .await()

                if (!snapshot.exists()) {
                    LicenseResult.InvalidCode
                } else {

                    val existingDevice =
                        snapshot
                            .child("deviceId")
                            .getValue(String::class.java)

                    val redeemed =
                        snapshot
                            .child("redeemed")
                            .getValue(Boolean::class.java)
                            ?: false

                    val enabled =
                        snapshot
                            .child("enabled")
                            .getValue(Boolean::class.java)
                            ?: false

                    val expiresAt =
                        snapshot
                            .child("expiresAt")
                            .getValue(Long::class.java)
                            ?: 0L

                    when {

                        !enabled ->
                            LicenseResult.Disabled

                        expiresAt > 0L &&
                            System.currentTimeMillis() >
                            expiresAt ->
                            LicenseResult.Expired

                        redeemed &&
                            existingDevice != deviceId ->
                            LicenseResult.AlreadyBound

                        redeemed &&
                            existingDevice == deviceId ->
                            LicenseResult.AlreadyBound

                        else ->
                            LicenseResult.InvalidCode
                    }
                }

            } else {
                LicenseResult.Success
            }

        } catch (exception: Exception) {

            LicenseResult.Error(
                exception.message
                    ?: "Unable to contact license server"
            )
        }
    }
}
package com.asimofficial.gameutility.util

import android.content.Context
import android.content.pm.ApplicationInfo
import android.content.pm.PackageManager
import com.asimofficial.gameutility.model.GameApp

object GameDetector {

    fun getInstalledGames(
        context: Context
    ): List<GameApp> {

        val packageManager =
            context.packageManager

        return packageManager
            .getInstalledApplications(
                PackageManager.GET_META_DATA
            )
            .asSequence()
            .filter { applicationInfo ->

                val launchIntent =
                    packageManager
                        .getLaunchIntentForPackage(
                            applicationInfo.packageName
                        )

                launchIntent != null
            }
            .filter { applicationInfo ->

                val isGameCategory =
                    applicationInfo.category ==
                        ApplicationInfo.CATEGORY_GAME

                val packageName =
                    applicationInfo.packageName
                        .lowercase()

                val knownGame =
                    KNOWN_GAME_KEYWORDS.any {
                        packageName.contains(it)
                    }

                isGameCategory || knownGame
            }
            .map { applicationInfo ->

                GameApp(
                    packageName =
                        applicationInfo.packageName,

                    appName =
                        packageManager
                            .getApplicationLabel(
                                applicationInfo
                            )
                            .toString(),

                    icon =
                        packageManager
                            .getApplicationIcon(
                                applicationInfo
                            )
                )
            }
            .distinctBy {
                it.packageName
            }
            .sortedBy {
                it.appName.lowercase()
            }
            .toList()
    }

    private val KNOWN_GAME_KEYWORDS =
        setOf(
            "freefire",
            "freefiremax",
            "pubg",
            "bgmi",
            "callofduty",
            "codmobile",
            "mobilelegends",
            "clashofclans",
            "clashroyale",
            "minecraft",
            "roblox",
            "fortnite",
            "asphalt",
            "efootball",
            "football",
            "gameloft",
            "garena",
            "supercell",
            "netease",
            "krafton",
            "activision"
        )
}
package com.asimofficial.gameutility.ui

import android.view.LayoutInflater
import android.view.ViewGroup
import androidx.recyclerview.widget.DiffUtil
import androidx.recyclerview.widget.ListAdapter
import androidx.recyclerview.widget.RecyclerView
import com.asimofficial.gameutility.databinding.ItemGameBinding
import com.asimofficial.gameutility.model.GameApp

class GameAdapter(
    private val onGameClicked: (GameApp) -> Unit
) : ListAdapter<GameApp, GameAdapter.GameViewHolder>(
    DIFF_CALLBACK
) {

    override fun onCreateViewHolder(
        parent: ViewGroup,
        viewType: Int
    ): GameViewHolder {

        val binding =
            ItemGameBinding.inflate(
                LayoutInflater.from(parent.context),
                parent,
                false
            )

        return GameViewHolder(binding)
    }

    override fun onBindViewHolder(
        holder: GameViewHolder,
        position: Int
    ) {
        holder.bind(getItem(position))
    }

    inner class GameViewHolder(
        private val binding: ItemGameBinding
    ) : RecyclerView.ViewHolder(
        binding.root
    ) {

        fun bind(game: GameApp) {

            binding.gameName.text =
                game.appName

            binding.packageName.text =
                game.packageName

            binding.gameIcon.setImageDrawable(
                game.icon
            )

            binding.root.setOnClickListener {
                onGameClicked(game)
            }
        }
    }

    companion object {

        private val DIFF_CALLBACK =
            object :
                DiffUtil.ItemCallback<GameApp>() {

                override fun areItemsTheSame(
                    oldItem: GameApp,
                    newItem: GameApp
                ): Boolean {

                    return oldItem.packageName ==
                        newItem.packageName
                }

                override fun areContentsTheSame(
                    oldItem: GameApp,
                    newItem: GameApp
                ): Boolean {

                    return oldItem ==
                        newItem
                }
            }
    }
}
package com.asimofficial.gameutility.ui

import android.content.Intent
import android.os.Bundle
import android.provider.Settings
import android.widget.Toast
import androidx.appcompat.app.AppCompatActivity
import androidx.lifecycle.lifecycleScope
import com.asimofficial.gameutility.data.LicenseRepository
import com.asimofficial.gameutility.data.LicenseResult
import com.asimofficial.gameutility.data.SessionManager
import com.asimofficial.gameutility.databinding.ActivityLoginBinding
import kotlinx.coroutines.launch

class LoginActivity : AppCompatActivity() {

    private lateinit var binding:
        ActivityLoginBinding

    private lateinit var sessionManager:
        SessionManager

    private lateinit var repository:
        LicenseRepository

    override fun onCreate(
        savedInstanceState: Bundle?
    ) {
        super.onCreate(savedInstanceState)

        sessionManager =
            SessionManager(this)

        if (sessionManager.isLoggedIn()) {
            openHome()
            return
        }

        binding =
            ActivityLoginBinding.inflate(
                layoutInflater
            )

        setContentView(binding.root)

        repository =
            LicenseRepository()

        binding.submitButton.setOnClickListener {
            redeem()
        }
    }

    private fun redeem() {

        val code =
            binding.redeemCodeEditText
                .text
                .toString()
                .trim()

        if (code.isBlank()) {

            binding.redeemCodeEditText.error =
                "Enter your redeem code"

            return
        }

        binding.submitButton.isEnabled =
            false

        binding.progressBar.visibility =
            android.view.View.VISIBLE

        val deviceId =
            Settings.Secure.getString(
                contentResolver,
                Settings.Secure.ANDROID_ID
            )

        if (deviceId.isNullOrBlank()) {

            showError(
                "Unable to identify this device"
            )

            return
        }

        lifecycleScope.launch {

            val result =
                repository.redeemCode(
                    code = code,
                    deviceId = deviceId
                )

            when (result) {

                LicenseResult.Success -> {

                    sessionManager
                        .saveSession(code)

                    openHome()
                }

                LicenseResult.InvalidCode -> {

                    showError(
                        "Invalid redeem code"
                    )
                }

                LicenseResult.AlreadyBound -> {

                    showError(
                        "Code already bound to another device"
                    )
                }

                LicenseResult.Expired -> {

                    showError(
                        "This code has expired"
                    )
                }

                LicenseResult.Disabled -> {

                    showError(
                        "This code is disabled"
                    )
                }

                is LicenseResult.Error -> {

                    showError(
                        result.message
                    )
                }
            }
        }
    }

    private fun showError(
        message: String
    ) {

        binding.submitButton.isEnabled =
            true

        binding.progressBar.visibility =
            android.view.View.GONE

        Toast.makeText(
            this,
            message,
            Toast.LENGTH_LONG
        ).show()
    }

    private fun openHome() {

        startActivity(
            Intent(
                this,
                HomeActivity::class.java
            )
        )

        finish()
    }
}
package com.asimofficial.gameutility.ui

import android.content.Intent
import android.net.Uri
import android.os.Bundle
import android.provider.Settings
import android.widget.Toast
import androidx.activity.result.contract.ActivityResultContracts
import androidx.appcompat.app.AppCompatActivity
import androidx.core.content.ContextCompat
import com.asimofficial.gameutility.databinding.ActivityHomeBinding
import com.asimofficial.gameutility.model.GameApp
import com.asimofficial.gameutility.service.OverlayService
import com.asimofficial.gameutility.util.GameDetector

class HomeActivity : AppCompatActivity() {

    private lateinit var binding:
        ActivityHomeBinding

    private lateinit var adapter:
        GameAdapter

    private val selectedPackageLauncher =
        registerForActivityResult(
            ActivityResultContracts
                .StartActivityForResult()
        ) {
            loadGames()
        }

    override fun onCreate(
        savedInstanceState: Bundle?
    ) {
        super.onCreate(savedInstanceState)

        binding =
            ActivityHomeBinding.inflate(
                layoutInflater
            )

        setContentView(binding.root)

        adapter =
            GameAdapter { game ->
                launchGame(game)
            }

        binding.gamesRecyclerView.adapter =
            adapter

        binding.addButton.setOnClickListener {
            openAppSettings()
        }

        binding.overlayPermissionButton
            .setOnClickListener {
                requestOverlayPermission()
            }

        loadGames()
    }

    override fun onResume() {
        super.onResume()

        updateOverlayPermissionUI()
        loadGames()
    }

    private fun loadGames() {

        val games =
            GameDetector
                .getInstalledGames(this)

        adapter.submitList(games)

        binding.emptyView.visibility =
            if (games.isEmpty()) {
                android.view.View.VISIBLE
            } else {
                android.view.View.GONE
            }
    }

    private fun launchGame(
        game: GameApp
    ) {

        if (!Settings.canDrawOverlays(this)) {

            requestOverlayPermission()

            Toast.makeText(
                this,
                "Allow overlay permission first",
                Toast.LENGTH_LONG
            ).show()

            return
        }

        val launchIntent =
            packageManager
                .getLaunchIntentForPackage(
                    game.packageName
                )

        if (launchIntent == null) {

            Toast.makeText(
                this,
                "Unable to launch ${game.appName}",
                Toast.LENGTH_SHORT
            ).show()

            return
        }

        val serviceIntent =
            Intent(
                this,
                OverlayService::class.java
            )

        ContextCompat
            .startForegroundService(
                this,
                serviceIntent
            )

        launchIntent.addFlags(
            Intent.FLAG_ACTIVITY_NEW_TASK
        )

        startActivity(launchIntent)
    }

    private fun requestOverlayPermission() {

        if (Settings.canDrawOverlays(this)) {
            return
        }

        val intent =
            Intent(
                Settings.ACTION_MANAGE_OVERLAY_PERMISSION,
                Uri.parse(
                    "package:$packageName"
                )
            )

        selectedPackageLauncher.launch(intent)
    }

    private fun updateOverlayPermissionUI() {

        val allowed =
            Settings.canDrawOverlays(this)

        binding.overlayStatus.text =
            if (allowed) {
                "Overlay permission: ENABLED"
            } else {
                "Overlay permission: REQUIRED"
            }
    }

    private fun openAppSettings() {

        /*
         * Android does not expose a universal "pick any installed
         * application" contract on every supported device.
         *
         * The application settings screen provides a safe manual
         * route. Automatically detected games remain in the list.
         */
        val intent =
            Intent(
                Settings.ACTION_MANAGE_APPLICATIONS_SETTINGS
            )

        startActivity(intent)
    }
}
package com.asimofficial.gameutility.service

import android.app.Notification
import android.app.NotificationChannel
import android.app.NotificationManager
import android.app.Service
import android.content.Intent
import android.graphics.PixelFormat
import android.os.Build
import android.os.IBinder
import android.provider.Settings
import android.view.Gravity
import android.view.LayoutInflater
import android.view.MotionEvent
import android.view.View
import android.view.WindowManager
import android.widget.ImageButton
import android.widget.TextView
import android.widget.Toast
import androidx.core.app.NotificationCompat
import com.asimofficial.gameutility.R
import kotlin.math.roundToInt

class OverlayService : Service() {

    companion object {

        private const val CHANNEL_ID =
            "asim_overlay_service"

        private const val NOTIFICATION_ID =
            5001
    }

    private lateinit var windowManager:
        WindowManager

    private var overlayView:
        View? = null

    private var windowParams:
        WindowManager.LayoutParams? = null

    private var locked = false

    private var initialX = 0
    private var initialY = 0

    private var initialTouchX = 0f
    private var initialTouchY = 0f

    private var downTime = 0L

    override fun onCreate() {
        super.onCreate()

        createNotificationChannel()

        startForeground(
            NOTIFICATION_ID,
            createNotification()
        )

        if (!Settings.canDrawOverlays(this)) {

            stopSelf()

            return
        }

        createOverlay()
    }

    private fun createOverlay() {

        windowManager =
            getSystemService(
                WINDOW_SERVICE
            ) as WindowManager

        val view =
            LayoutInflater
                .from(this)
                .inflate(
                    R.layout.overlay_view,
                    null
                )

        overlayView = view

        val macroButton =
            view.findViewById<View>(
                R.id.macroButton
            )

        val lockButton =
            view.findViewById<ImageButton>(
                R.id.lockButton
            )

        val lockLabel =
            view.findViewById<TextView>(
                R.id.lockLabel
            )

        windowParams =
            WindowManager.LayoutParams(
                dp(82),
                dp(82),
                WindowManager.LayoutParams
                    .TYPE_APPLICATION_OVERLAY,
                WindowManager.LayoutParams
                    .FLAG_NOT_FOCUSABLE or
                    WindowManager.LayoutParams
                    .FLAG_LAYOUT_NO_LIMITS,
                PixelFormat.TRANSLUCENT
            ).apply {

                gravity =
                    Gravity.TOP or Gravity.START

                x = dp(24)
                y = dp(260)
            }

        lockButton.setOnClickListener {

            locked = !locked

            if (locked) {

                lockButton.setImageResource(
                    R.drawable.ic_lock
                )

                lockLabel.text =
                    "LOCKED"

                lockLabel.visibility =
                    View.VISIBLE

            } else {

                lockButton.setImageResource(
                    R.drawable.ic_unlock
                )

                lockLabel.text =
                    "MOVE"

                lockLabel.visibility =
                    View.GONE
            }
        }

        macroButton.setOnTouchListener { _, event ->

            if (locked) {
                return@setOnTouchListener true
            }

            when (event.actionMasked) {

                MotionEvent.ACTION_DOWN -> {

                    downTime =
                        System.currentTimeMillis()

                    initialX =
                        windowParams!!.x

                    initialY =
                        windowParams!!.y

                    initialTouchX =
                        event.rawX

                    initialTouchY =
                        event.rawY

                    true
                }

                MotionEvent.ACTION_MOVE -> {

                    val deltaX =
                        (
                            event.rawX -
                                initialTouchX
                            ).roundToInt()

                    val deltaY =
                        (
                            event.rawY -
                                initialTouchY
                            ).roundToInt()

                    windowParams!!.x =
                        initialX + deltaX

                    windowParams!!.y =
                        initialY + deltaY

                    constrainPosition()

                    try {

                        windowManager
                            .updateViewLayout(
                                view,
                                windowParams
                            )

                    } catch (
                        exception: Exception
                    ) {
                        stopSelf()
                    }

                    true
                }

                MotionEvent.ACTION_UP -> {

                    val duration =
                        System.currentTimeMillis() -
                            downTime

                    /*
                     * The macro button deliberately does not
                     * perform automated game actions.
                     * It is a movable HUD control.
                     */

                    duration >= 0L

                    true
                }

                MotionEvent.ACTION_CANCEL -> true

                else -> false
            }
        }

        try {

            windowManager.addView(
                view,
                windowParams
            )

        } catch (
            exception: Exception
        ) {

            Toast.makeText(
                this,
                "Unable to create overlay",
                Toast.LENGTH_LONG
            ).show()

            stopSelf()
        }
    }

    private fun constrainPosition() {

        val displayMetrics =
            resources.displayMetrics

        val screenWidth =
            displayMetrics.widthPixels

        val screenHeight =
            displayMetrics.heightPixels

        val overlayWidth =
            windowParams!!.width

        val overlayHeight =
            windowParams!!.height

        windowParams!!.x =
            windowParams!!.x.coerceIn(
                0,
                (screenWidth - overlayWidth)
                    .coerceAtLeast(0)
            )

        windowParams!!.y =
            windowParams!!.y.coerceIn(
                0,
                (screenHeight - overlayHeight)
                    .coerceAtLeast(0)
            )
    }

    override fun onStartCommand(
        intent: Intent?,
        flags: Int,
        startId: Int
    ): Int {

        return START_STICKY
    }

    override fun onDestroy() {

        overlayView?.let { view ->

            try {
                windowManager.removeView(view)
            } catch (_: Exception) {
            }
        }

        overlayView = null

        super.onDestroy()
    }

    override fun onBind(
        intent: Intent?
    ): IBinder? {
        return null
    }

    private fun dp(
        value: Int
    ): Int {

        return (
            value *
                resources.displayMetrics.density
            ).roundToInt()
    }

    private fun createNotificationChannel() {

        if (
            Build.VERSION.SDK_INT >=
            Build.VERSION_CODES.O
        ) {

            val channel =
                NotificationChannel(
                    CHANNEL_ID,
                    "ASIM OFFICIAL Overlay",
                    NotificationManager
                        .IMPORTANCE_LOW
                ).apply {

                    description =
                        "Game utility overlay service"

                    setShowBadge(false)
                }

            val manager =
                getSystemService(
                    NotificationManager::class.java
                )

            manager.createNotificationChannel(
                channel
            )
        }
    }

    private fun createNotification():
        Notification {

        return NotificationCompat
            .Builder(
                this,
                CHANNEL_ID
            )
            .setSmallIcon(
                R.drawable.ic_game
            )
            .setContentTitle(
                "ASIM OFFICIAL"
            )
            .setContentText(
                "Game overlay is active"
            )
            .setOngoing(true)
            .setCategory(
                NotificationCompat
                    .CATEGORY_SERVICE
            )
            .setPriority(
                NotificationCompat
                    .PRIORITY_LOW
            )
            .build()
    }
}
<?xml version="1.0" encoding="utf-8"?>

<ScrollView
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:fillViewport="true"
    android:background="@color/background">

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical"
        android:padding="24dp">

        <TextView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginTop="32dp"
            android:gravity="center"
            android:text="ASIM OFFICIAL"
            android:textColor="@color/white"
            android:textSize="32sp"
            android:textStyle="bold"
            android:letterSpacing="0.08" />

        <TextView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginTop="8dp"
            android:gravity="center"
            android:text="GAME UTILITY OVERLAY MANAGER"
            android:textColor="@color/text_secondary"
            android:textSize="12sp"
            android:textStyle="bold"
            android:letterSpacing="0.12" />

        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginTop="28dp"
            android:orientation="vertical"
            android:padding="20dp"
            android:background="@drawable/bg_app">

            <TextView
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="UNLOCK ACCESS"
                android:textColor="@color/white"
                android:textSize="18sp"
                android:textStyle="bold" />

            <TextView
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:layout_marginTop="6dp"
                android:text="Purchase an access code and enter it below."
                android:textColor="@color/text_secondary"
                android:textSize="13sp" />

            <LinearLayout
                android:layout_width="match_parent"
                android:layout_height="220dp"
                android:layout_marginTop="18dp"
                android:gravity="center"
                android:orientation="vertical"
                android:background="@drawable/bg_qr">

                <TextView
                    android:layout_width="wrap_content"
                    android:layout_height="wrap_content"
                    android:text="UPI / PHONEPE"
                    android:textColor="@color/white"
                    android:textSize="18sp"
                    android:textStyle="bold" />

                <TextView
                    android:layout_width="wrap_content"
                    android:layout_height="wrap_content"
                    android:layout_marginTop="10dp"
                    android:text="Support: 9907958709"
                    android:textColor="@color/accent"
                    android:textSize="16sp"
                    android:textStyle="bold" />

                <TextView
                    android:layout_width="wrap_content"
                    android:layout_height="wrap_content"
                    android:layout_marginTop="12dp"
                    android:text="Contact support for payment details"
                    android:textColor="@color/text_secondary"
                    android:textSize="12sp" />

            </LinearLayout>

            <com.google.android.material.textfield.TextInputLayout
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:layout_marginTop="22dp"
                android:hint="Redeem Code / Password"
                app:boxBackgroundMode="outline"
                app:boxStrokeColor="@color/accent"
                app:hintTextColor="@color/text_secondary">

                <com.google.android.material.textfield.TextInputEditText
                    android:id="@+id/redeemCodeEditText"
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:inputType="textPassword"
                    android:textColor="@color/white"
                    android:textColorHint="@color/text_secondary" />

            </com.google.android.material.textfield.TextInputLayout>

            <com.google.android.material.button.MaterialButton
                android:id="@+id/submitButton"
                android:layout_width="match_parent"
                android:layout_height="56dp"
                android:layout_marginTop="18dp"
                android:text="SUBMIT / UNLOCK"
                android:textStyle="bold"
                android:textColor="@color/black"
                app:backgroundTint="@color/accent" />

            <ProgressBar
                android:id="@+id/progressBar"
                android:layout_width="32dp"
                android:layout_height="32dp"
                android:layout_gravity="center"
                android:layout_marginTop="16dp"
                android:visibility="gone" />

        </LinearLayout>

    </LinearLayout>

</ScrollView>
<?xml version="1.0" encoding="utf-8"?>

<androidx.constraintlayout.widget.ConstraintLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="@color/background">

    <TextView
        android:id="@+id/title"
        android:layout_width="0dp"
        android:layout_height="wrap_content"
        android:layout_marginStart="20dp"
        android:layout_marginTop="24dp"
        android:text="ASIM OFFICIAL"
        android:textColor="@color/white"
        android:textSize="28sp"
        android:textStyle="bold"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <TextView
        android:id="@+id/subtitle"
        android:layout_width="0dp"
        android:layout_height="wrap_content"
        android:layout_marginStart="20dp"
        android:layout_marginTop="4dp"
        android:text="YOUR GAME UTILITY DASHBOARD"
        android:textColor="@color/text_secondary"
        android:textSize="11sp"
        android:textStyle="bold"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@id/title" />

    <ImageButton
        android:id="@+id/addButton"
        android:layout_width="52dp"
        android:layout_height="52dp"
        android:layout_marginEnd="20dp"
        android:background="@drawable/bg_button"
        android:contentDescription="Add application"
        android:padding="14dp"
        android:src="@drawable/ic_add"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintTop_toTopOf="@id/title" />

    <TextView
        android:id="@+id/overlayStatus"
        android:layout_width="0dp"
        android:layout_height="wrap_content"
        android:layout_marginStart="20dp"
        android:layout_marginTop="22dp"
        android:text="Overlay permission: REQUIRED"
        android:textColor="@color/accent"
        android:textSize="13sp"
        android:textStyle="bold"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@id/subtitle" />

    <com.google.android.material.button.MaterialButton
        android:id="@+id/overlayPermissionButton"
        android:layout_width="wrap_content"
        android:layout_height="46dp"
        android:layout_marginEnd="20dp"
        android:text="OVERLAY SETTINGS"
        android:textSize="11sp"
        android:textStyle="bold"
        app:backgroundTint="@color/card"
        app:layout_constraintBottom_toBottomOf="@id/overlayStatus"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintTop_toTopOf="@id/overlayStatus" />

    <androidx.recyclerview.widget.RecyclerView
        android:id="@+id/gamesRecyclerView"
        android:layout_width="0dp"
        android:layout_height="0dp"
        android:layout_marginTop="20dp"
        android:clipToPadding="false"
        android:paddingStart="16dp"
        android:paddingEnd="16dp"
        android:paddingBottom="24dp"
        app:layoutManager="androidx.recyclerview.widget.LinearLayoutManager"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@id/overlayStatus" />

    <TextView
        android:id="@+id/emptyView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="No games detected"
        android:textColor="@color/text_secondary"
        android:textSize="15sp"
        android:visibility="gone"
        app:layout_constraintBottom_toBottomOf="@id/gamesRecyclerView"
        app:layout_constraintEnd_toEndOf="@id/gamesRecyclerView"
        app:layout_constraintStart_toStartOf="@id/gamesRecyclerView"
        app:layout_constraintTop_toTopOf="@id/gamesRecyclerView" />

</androidx.constraintlayout.widget.ConstraintLayout>
implementation(
    "androidx.constraintlayout:constraintlayout:2.2.0"
)
<?xml version="1.0" encoding="utf-8"?>

<com.google.android.material.card.MaterialCardView
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="82dp"
    android:layout_marginBottom="10dp"
    app:cardBackgroundColor="@color/card"
    app:cardCornerRadius="18dp"
    app:cardElevation="0dp"
    app:strokeColor="@color/stroke"
    app:strokeWidth="1dp">

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:gravity="center_vertical"
        android:orientation="horizontal"
        android:padding="12dp">

        <ImageView
            android:id="@+id/gameIcon"
            android:layout_width="54dp"
            android:layout_height="54dp"
            android:contentDescription="Game icon"
            android:scaleType="centerCrop" />

        <LinearLayout
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_marginStart="14dp"
            android:layout_weight="1"
            android:orientation="vertical">

            <TextView
                android:id="@+id/gameName"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:ellipsize="end"
                android:maxLines="1"
                android:textColor="@color/white"
                android:textSize="16sp"
                android:textStyle="bold" />

            <TextView
                android:id="@+id/packageName"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:layout_marginTop="4dp"
                android:ellipsize="end"
                android:maxLines="1"
                android:textColor="@color/text_secondary"
                android:textSize="11sp" />

        </LinearLayout>

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="PLAY"
            android:textColor="@color/accent"
            android:textSize="11sp"
            android:textStyle="bold" />

    </LinearLayout>

</com.google.android.material.card.MaterialCardView>
<?xml version="1.0" encoding="utf-8"?>

<FrameLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="82dp"
    android:layout_height="82dp">

    <ImageButton
        android:id="@+id/macroButton"
        android:layout_width="68dp"
        android:layout_height="68dp"
        android:layout_gravity="center"
        android:background="@drawable/bg_overlay"
        android:contentDescription="ASIM OFFICIAL HUD"
        android:padding="18dp"
        android:src="@drawable/ic_game" />

    <ImageButton
        android:id="@+id/lockButton"
        android:layout_width="28dp"
        android:layout_height="28dp"
        android:layout_gravity="top|end"
        android:background="@drawable/bg_overlay_lock"
        android:contentDescription="Lock overlay"
        android:padding="6dp"
        android:src="@drawable/ic_unlock" />

    <TextView
        android:id="@+id/lockLabel"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_gravity="bottom|center_horizontal"
        android:background="@drawable/bg_overlay_lock"
        android:paddingStart="5dp"
        android:paddingEnd="5dp"
        android:text="LOCKED"
        android:textColor="@color/white"
        android:textSize="7sp"
        android:textStyle="bold"
        android:visibility="gone" />

</FrameLayout>
<?xml version="1.0" encoding="utf-8"?>

<resources>

    <color name="background">#08090C</color>
    <color name="card">#111318</color>
    <color name="card_light">#171A21</color>
    <color name="stroke">#272B34</color>

    <color name="accent">#00E5FF</color>
    <color name="accent_dark">#00AFC2</color>

    <color name="white">#FFFFFF</color>
    <color name="black">#000000</color>

    <color name="text_secondary">#9298A5</color>

</resources>
<?xml version="1.0" encoding="utf-8"?>

<resources>

    <style
        name="Theme.ASIMOfficial"
        parent="Theme.Material3.Dark.NoActionBar">

        <item name="android:fontFamily">sans</item>

        <item name="android:windowLightStatusBar">
            false
        </item>

        <item name="android:statusBarColor">
            @color/background
        </item>

        <item name="android:navigationBarColor">
            @color/background
        </item>

        <item name="android:windowActionModeOverlay">
            true
        </item>

        <item name="colorPrimary">
            @color/accent
        </item>

        <item name="colorSecondary">
            @color/accent
        </item>

    </style>

</resources>
<?xml version="1.0" encoding="utf-8"?>

<shape
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:shape="rectangle">

    <solid
        android:color="@color/card" />

    <corners
        android:radius="22dp" />

    <stroke
        android:width="1dp"
        android:color="@color/stroke" />

</shape>
<?xml version="1.0" encoding="utf-8"?>

<shape
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:shape="rectangle">

    <solid
        android:color="@color/accent" />

    <corners
        android:radius="16dp" />

</shape>
<?xml version="1.0" encoding="utf-8"?>

<shape
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:shape="rectangle">

    <solid
        android:color="@color/card" />

    <corners
        android:radius="18dp" />

</shape>
<?xml version="1.0" encoding="utf-8"?>

<shape
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:shape="rectangle">

    <solid
        android:color="@color/card_light" />

    <corners
        android:radius="18dp" />

    <stroke
        android:width="1dp"
        android:color="@color/stroke" />

</shape>
<?xml version="1.0" encoding="utf-8"?>

<shape
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:shape="oval">

    <solid
        android:color="#E6000000" />

    <stroke
        android:width="2dp"
        android:color="@color/accent" />

</shape>
<?xml version="1.0" encoding="utf-8"?>

<shape
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:shape="oval">

    <solid
        android:color="#E61A1D24" />

    <stroke
        android:width="1dp"
        android:color="@color/accent" />

</shape>
<vector
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:width="24dp"
    android:height="24dp"
    android:viewportWidth="24"
    android:viewportHeight="24">

    <path
        android:fillColor="#000000"
        android:pathData="M19,13H13V19H11V13H5V11H11V5H13V11H19V13Z" />

</vector>
<vector
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:width="48dp"
    android:height="48dp"
    android:viewportWidth="48"
    android:viewportHeight="48">

    <path
        android:fillColor="#00E5FF"
        android:pathData="M15,14h18c5,0 8,4 8,9v6c0,4 -3,6 -6,4l-5,-4H18l-5,4c-3,2 -6,0 -6,-4v-6c0,-5 3,-9 8,-9z" />

    <path
        android:fillColor="#08090C"
        android:pathData="M15,21h3v-3h2v3h3v2h-3v3h-2v-3h-3z" />

    <path
        android:fillColor="#08090C"
        android:pathData="M31,20m-2,0a2,2 0,1 0,4 0a2,2 0,1 0,-4 0" />

    <path
        android:fillColor="#08090C"
        android:pathData="M35,24m-2,0a2,2 0,1 0,4 0a2,2 0,1 0,-4 0" />

</vector>
<vector
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:width="24dp"
    android:height="24dp"
    android:viewportWidth="24"
    android:viewportHeight="24">

    <path
        android:fillColor="#FFFFFF"
        android:pathData="M17,8H16V6C16,3.79 14.21,2 12,2C9.79,2 8,3.79 8,6V8H7C5.9,8 5,8.9 5,10V20C5,21.1 5.9,22 7,22H17C18.1,22 19,21.1 19,20V10C19,8.9 18.1,8 17,8M10,6C10,4.9 10.9,4 12,4C13.1,4 14,4.9 14,6V8H10V6M17,20H7V10H17V20M12,17C13.1,17 14,16.1 14,15C14,13.9 13.1,13 12,13C10.9,13 10,13.9 10,15C10,16.1 10.9,17 12,17Z" />

</vector>
<vector
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:width="24dp"
    android:height="24dp"
    android:viewportWidth="24"
    android:viewportHeight="24">

    <path
        android:fillColor="#FFFFFF"
        android:pathData="M18,8H10V6C10,4.9 10.9,4 12,4C13.1,4 14,4.9 14,6H16C16,3.79 14.21,2 12,2C9.79,2 8,3.79 8,6V8H6C4.9,8 4,8.9 4,10V20C4,21.1 4.9,22 6,22H18C19.1,22 20,21.1 20,20V10C20,8.9 19.1,8 18,8M18,20H6V10H18V20M12,17C13.1,17 14,16.1 14,15C14,13.9 13.1,13 12,13C10.9,13 10,13.9 10,15C10,16.1 10.9,17 12,17Z" />

</vector>
redeemCodes
└── ASIM-2026-ABC123
    ├── enabled: true
    ├── redeemed: false
    ├── deviceId: ""
    ├── redeemedAt: 0
    └── expiresAt: 0
redeemCodes
└── ASIM-2026-ABC123
    ├── enabled: true
    ├── redeemed: true
    ├── deviceId: "device-specific-ANDROID-ID"
    ├── redeemedAt: 178781...
    └── expiresAt: 0
read code
↓
check unused
↓
write used
{
  "rules": {
    "redeemCodes": {
      "$code": {
        ".read": true,
        ".write": false
      }
    }
  }
}
ASIM OFFICIAL APK
        │
        │ HTTPS
        ▼
Authentication / License API
        │
        ▼
Firebase / secure database
        │
        ├── validate code
        ├── check expiration
        ├── check redeemed
        ├── check device binding
        └── atomically claim code
SUCCESS
INVALID_CODE
ALREADY_BOUND
EXPIRED
DISABLED
