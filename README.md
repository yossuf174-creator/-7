import React from "react";
import { NavigationContainer } from "@react-navigation/native";
import { createBottomTabNavigator } from "@react-navigation/bottom-tabs";
import { View, Text, StyleSheet } from "react-native";

const Tab = createBottomTabNavigator();

function HomeScreen() {
  return (
    <View style={styles.container}>
      <Text style={styles.title}>🔥 ABK Home</Text>
    </View>
  );
}

function DownloadScreen() {
  return (
    <View style={styles.container}>
      <Text style={styles.title}>📥 تحميل الفيديو</Text>
    </View>
  );
}

function DesignScreen() {
  return (
    <View style={styles.container}>
      <Text style={styles.title}>🎨 التصميم</Text>
    </View>
  );
}

function BotScreen() {
  return (
    <View style={styles.container}>
      <Text style={styles.title}>🤖 البوت</Text>
    </View>
  );
}

export default function App() {
  return (
    <NavigationContainer>
      <Tab.Navigator screenOptions={{ headerShown: false }}>
        <Tab.Screen name="Home" component={HomeScreen} />
        <Tab.Screen name="Download" component={DownloadScreen} />
        <Tab.Screen name="Design" component={DesignScreen} />
        <Tab.Screen name="Bot" component={BotScreen} />
      </Tab.Navigator>
    </NavigationContainer>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: "#020617",
    justifyContent: "center",
    alignItems: "center",
  },
  title: {
    color: "#fff",
    fontSize: 24,
  },
});
