################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32L0xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
part3_BlinkyLED.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
part3_BlinkyLED.list \

OBJCOPY_BIN += \
part3_BlinkyLED.bin \


# All Target
all: part3_BlinkyLED.elf secondary-outputs

# Tool invocations
part3_BlinkyLED.elf: $(OBJS) $(USER_OBJS) C:\Users\haing\Desktop\LearningSTM32Blog\part3_BlinkyLED\STM32L053R8TX_FLASH.ld
	arm-none-eabi-gcc -o "part3_BlinkyLED.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m0plus -T"C:\Users\haing\Desktop\LearningSTM32Blog\part3_BlinkyLED\STM32L053R8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="part3_BlinkyLED.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

part3_BlinkyLED.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "part3_BlinkyLED.list"
	@echo 'Finished building: $@'
	@echo ' '

part3_BlinkyLED.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "part3_BlinkyLED.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
