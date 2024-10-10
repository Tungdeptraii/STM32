################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (12.3.rel1)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

OPTIONAL_TOOL_DEPS := \
$(wildcard ../makefile.defs) \
$(wildcard ../makefile.init) \
$(wildcard ../makefile.targets) \


BUILD_ARTIFACT_NAME := b4_input-captrue_output-compare
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
b4_input-captrue_output-compare.elf \

MAP_FILES += \
b4_input-captrue_output-compare.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
b4_input-captrue_output-compare.list \

OBJCOPY_HEX += \
b4_input-captrue_output-compare.hex \

OBJCOPY_BIN += \
b4_input-captrue_output-compare.bin \


# All Target
all: main-build

# Main-build Target
main-build: b4_input-captrue_output-compare.elf secondary-outputs

# Tool invocations
b4_input-captrue_output-compare.elf b4_input-captrue_output-compare.map: $(OBJS) $(USER_OBJS) D:\STM32CubeIDE\workspace_1.15.1\b4_input-captrue_output-compare\STM32F103C8TX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "b4_input-captrue_output-compare.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"D:\STM32CubeIDE\workspace_1.15.1\b4_input-captrue_output-compare\STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="b4_input-captrue_output-compare.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

b4_input-captrue_output-compare.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "b4_input-captrue_output-compare.list"
	@echo 'Finished building: $@'
	@echo ' '

b4_input-captrue_output-compare.hex: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "b4_input-captrue_output-compare.hex"
	@echo 'Finished building: $@'
	@echo ' '

b4_input-captrue_output-compare.bin: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "b4_input-captrue_output-compare.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) b4_input-captrue_output-compare.bin b4_input-captrue_output-compare.elf b4_input-captrue_output-compare.hex b4_input-captrue_output-compare.list b4_input-captrue_output-compare.map default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX) $(OBJCOPY_BIN)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
