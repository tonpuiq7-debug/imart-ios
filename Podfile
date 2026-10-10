# Uncomment the next line to define a global platform for your project
platform :ios, '15.0'

target 'imart' do
  # Comment the next line if you don't want to use dynamic frameworks
  use_frameworks!

  # Add the pod for Firebase Cloud Messaging (Firebase 10.x stable)
  pod 'Firebase/Messaging', '~> 10.29.0'

end

post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '15.0'
      config.build_settings['OTHER_SWIFT_FLAGS'] ||= ['$(inherited)']
      config.build_settings['OTHER_SWIFT_FLAGS'] << '-enable-experimental-feature'
      config.build_settings['OTHER_SWIFT_FLAGS'] << 'AccessLevelOnImport'
    end
  end
end